datasciencecoursera
===================

#Repo created for Data Scienctist's Toolkit project

##README

###Overview
The purpose of this project is to assess our ability to collect, work with, and clean a dataset. The assignment deliverables expected are as follows:

1. One R script called `run_analysis.R` that collects, transforms, cleans and creates a tidy dataset
2. A tidy dataset `tidy dataset.txt`, output from running the R script
3. A codebook called `codebook.md` that describes the variables, data and transformations performed
4. This `README.md` file that explains the R script
5. A Github repository to store the R script, codebook and README files

###run_analysis.R script
The run_analysis.R script is reproduced below together with explainations of the steps taken

Load data.table package
```
library(data.table)
```

<br/>Download the zipfile from url provided to local working directory. Extract folders & files to the sub-directory in the zipfile `/UCI HAR Dataset/`
```
src_url<-"http://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
download.file(src_url,destfile = "./Dataset.zip")
unzip("./Dataset.zip")
```

<br/>Read the `activity_labels.txt` and `features.txt` files into activity & features data.tables
```
activity<-fread("./UCI HAR Dataset/activity_labels.txt")
features<-fread("./UCI HAR Dataset/features.txt")
```

<br/>**Assignment Task 2** - Select mean and standard deviation measures

Since only the mean and standard deviation measures are needed, I decided to perform task 2 (find the mean & std variables) first, so that only these fields will be included when merging the training and test sets together (task 1)

My interpretation of the task 2 is to select only mean() & std() measures and so I have not included variables like XXX-meanFreq() and angle variables eg. angle(tBodyAccJerkMean),gravityMean)
```
selvar<-subset(features, grepl("mean()", features$V2, fixed=TRUE) | grepl("std()", features$V2, fixed=TRUE))
```

<br/>**Assignment Task 1** - Merge training and test datasets

Read in the training subject`subject_train.txt`, activity`y_train.txt` and measures`X_train.txt` files and create a training data.table with the subject, activity and mean/std variables
Using fread crashes RStudio so I had to first read the tables as data.frames and then convert them to data.table
```
traindata<-read.table("./UCI HAR Dataset/train/X_train.txt")
trainact<-read.table("./UCI HAR Dataset/train/y_train.txt")
trainsubj<-read.table("./UCI HAR Dataset/train/subject_train.txt")
trainset<-data.table(subject=unlist(trainsubj), activity=unlist(trainact), traindata[,selvar$V1])  #Inc Step 2
```

Do the same thing for the equivalent test datasets
```
testdata<-read.table("./UCI HAR Dataset/test/X_test.txt")
testact<-read.table("./UCI HAR Dataset/test/y_test.txt")
testsubj<-read.table("./UCI HAR Dataset/test/subject_test.txt")
testset<-data.table(subject=unlist(testsubj), activity=unlist(testact), testdata[,selvar$V1])
```

<br/>Combine the training and test data.tables together
```
combset<-rbindlist(list(trainset,testset))
```

<br/>**Assignment Task 3** - Replace activity code with descriptive names

Convert the activity code in the combined table into a factor, using the activity labels from the activity data.table
```
combset$activity<-factor(combset$activity,activity$V1, activity$V2)
```

<br/>**Assignment Task 4** - Label the dataset with descriptive names

I'm applying the rules according to the JL lecture, and expectations set by the TAs in course forums
- Rule 1 - Expand abbreviations - detailed expansion rules given below
- Rule 2 - Remove symbols eg. () and -
- Rule 3 - Convert names to lowercase

Instead of just replacing the columns names in the combined dataset, my approach is to first add a new column to the original variable name table (*selvar* which has already been filtered to retain only means & std variables) to store the longer descriptive name. This allows me to get back the original names easily if ever I needed to.

I then use the longer names to replace the column names in the combined dataset
```
selvar<-selvar[,desc:=V2]							#Add a new column for descriptive variable name
selvar$desc<-gsub('^t', 'time', selvar$desc) 			#Expand abbreviations - names starting with t to time
selvar$desc<-gsub('^f', 'frequency', selvar$desc) 			#Expand abbreviations - names starting with f to frequency
selvar$desc<-gsub('Acc', 'acceleration', selvar$desc) 		#Expand abbreviations - Acc to acceleration
selvar$desc<-gsub('Gyro', 'gyroscope', selvar$desc) 		#Expand abbreviations - Gyro to gyroscope
selvar$desc<-gsub('Mag', 'magnitute', selvar$desc) 		#Expand abbreviations - Mag  to magnitute
selvar$desc<-gsub('std', 'standardeviation', selvar$desc) 	#Expand abbreviations - std  to standarddeviation
selvar$desc<-gsub('BodyBody', 'body', selvar$desc) 		#Fix duplicated BodyBody mistake to body
selvar$desc<-gsub('-', '', selvar$desc) 				#Remove dash from name
selvar$desc<-gsub('()', '', selvar$desc, fixed = TRUE) 		#Remove () from name
selvar$desc<-tolower(selvar$desc) 					#convert to lowercase
setnames(combset,3:68,selvar$desc)					#Replace measure variable names(col 3-68) with descriptive name
```

<br/>**Assignment Task 5** - Create a new tidy dataset with the averages of each variable for each subject and activity

Used the .SD parameter to apply the mean function to all columns, except for the group by columns (indicated in the by=)
```
tidyset<-combset[,lapply(.SD, mean), by=list(subject,activity)]
setorder(tidyset,subject,activity)	#sorts the table by subject and activity
write.table(tidyset,file = "./tidy dataset.txt",row.names = FALSE)	#Delimitor character is space, same as the original files
```





##Codebook for Tidy_dataset.txt

###Original Dataset
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip


###Data Transformation
The original data set contains results of experiments carried by 30 volunteers - 21 for generating training data and 9 for generating test data, performing six activities wearing a Samsung Galaxy S II smartphone. Senor signal measurements were taken from the smartphone's embedded accelerometer and gyroscope on 561 features with time and frequency domain variables. The original dataset was segregated into 7 files
- README.txt | Overview of the experiment
- 'features_info.txt':   Information on the feature variables
- 'features.txt': List of all features measured, including the feature code and description
- 'activity_labels.txt': List of activity performed, including activity code and description
- 'train/X_train.txt': Measurements of each feature taken from the training data volunteers
- 'train/y_train.txt': Feature code corresponding to the measurement from the x_train.txt file
- 'test/X_test.txt': Measurements of each feature taken from the test data volunteers
- 'test/y_test.txt': Feature code corresponding to the measurement from the x_test.txt file

This dataset was transformed using R script **as.R**  as follows
- asd
- asd

> asd
> asdsdsd zxljk z;xc
> sdakj sldf

###Variables Description
| Variable Name | Description |
| --- | --- |
| subject | Identification number (from 1 to 30) of the subject who performed the activity. |
| activity | Activity performed by the subject. The activity labels are listed below together with the activity codes from the original dataset which have been replaced by the activity labels <ul><li> WALKING - 1</li><li> WALKING UPSTAIRS - 2</li><li> WALKING DOWNSTAIRS - 3</li><li> SITTING - 4</li><li> STANDING - 5</li><li> LAYING - 6</li></ul>|
| timebodyaccelerationmeanx | Average mean value (in Hertz) of the body acceleration signal, from the time domain, in direction X, for the subject & activity |
