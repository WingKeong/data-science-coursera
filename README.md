datasciencecoursera
===================

#Repo created for Data Scienctist's Toolkit project

##Codebook for Tidy_dataset.txt

###Original Dataset
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip


###Data Transformation
The original data set contains results of experiments carried by 30 volunteers - 21 for generating training data and 9 for generating test data, performing six activities wearing a Samsung Galaxy S II smartphone. Senor signal measurements were taken from the smartphone's embedded accelerometer and gyroscope on 561 features with time and frequency domain variables. The original dataset was segregated into 7 files
- 'README.txt':   Overview of the experiment
- 'features_info.txt':   Information on the feature variables
- 'features.txt': List of all features measured, including the feature code and description
- 'activity_labels.txt': List of activity performed, including activity code and description
- 'train/X_train.txt': Measurements of each feature taken from the training data volunteers
- 'train/y_train.txt': Feature code corresponding to the measurement from the x_train.txt file
- 'test/X_test.txt': Measurements of each feature taken from the test data volunteers
- 'test/y_test.txt': Feature code corresponding to the measurement from the x_test.txt file

This dataset was transformed 

###Variables Description
| Variable Name | Description |
| --- | --- |
| subject | Identification number (from 1 to 30) of the subject who performed the activity. |
| activity | Activity performed by the subject. The activity labels are listed below together with the activity codes from the original dataset which have been replaced by the activity labels <ul><li> WALKING - 1</li><li> WALKING UPSTAIRS - 2</li><li> WALKING DOWNSTAIRS - 3</li><li> SITTING - 4</li><li> STANDING - 5</li><li> LAYING - 6</li></ul>|
| timebodyaccelerationmeanx | Average mean value (in Hertz) of the body acceleration signal, from the time domain, in direction X, for the subject & activity |
