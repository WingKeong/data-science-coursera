datasciencecoursera
===================

#Repo created for Data Scienctist's Toolkit project

##README

###Overview
The purpose of this project is to assess our ability to collect, work with, and clean a dataset. The assignment deliverables are as follows:

1. One R script called *run_analysis.R* that collects, tranforms, cleans and creates a tidy dataset
2. A tidy dataset *"tidy dataset.txt"*, the output of the R script
3. A codebook called *"codebook.md"* that describes the variables, the data and transformations performed to clean up the data
4. This *README.md* file to explain the R script
5. A Github repository to store the R script, codebook and readme file

###run_analysis.R script
The run_analysis.R script is reproduced below together with explainations of the steps taken

Load data.table package
```
library(data.table)
```

Download zipfile from url provided to local working directory
Extract folders & files from the zipfile to the same sub-directory from the zipfile (/UCI HAR Dataset/ )
```
src_url<-"http://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
download.file(src_url,destfile = "./Dataset.zip")
unzip("./Dataset.zip")
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
