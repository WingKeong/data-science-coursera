datasciencecoursera
===================

#Repo created for Data Scienctist's Toolkit project

##Codebook for Tidy dataset.txt
test
>selvar<-selvar[,desc:=V2]
>selvar$desc<-gsub('^t', 'time', selvar$desc) #Expand abbreviations - t to time
>selvar$desc<-gsub('^f', 'frequency', selvar$desc) #Expand abbreviations - f to frequency


| Variable Name | Description |
| --- | --- |
| subject | Identification number of the subject who performed the activity |
| activity | Activity performed by the subject. The activity labels are listed below. The activity codes from the original dataset are not included in the tidy dataset file but are indicated against each label for reference <ul><li> WALKING - 1</li><li> WALKING UPSTAIRS - 2</li><li> WALKING DOWNSTAIRS - 3</li><li> SITTING - 4</li><li> STANDING - 5</li><li> LAYING - 6</li></ul>|
| timebodyaccelerationmeanx | Average mean value (in Hertz) of the body acceleration signal, from the time domain, in direction X, for the subject & activity |
| timebodyaccelerationmeany | Average mean value (in Hertz) of the body acceleration signal, from the time domain, in direction Y, for the subject & activity |
| timebodyaccelerationmeanz | Average mean value (in Hertz) of the body acceleration signal, from the time domain, in direction Z, for the subject & activity |
| timebodyaccelerationstandardeviationx | Average standard deviation (in Hertz) of the body acceleration signal, from the time domain, in direction X, for the subject & activity |
| timebodyaccelerationstandardeviationy | Average standard deviation (in Hertz) of the body acceleration signal, from the time domain, in direction Y, for the subject & activity |
| timebodyaccelerationstandardeviationz | Average standard deviation (in Hertz) of the body acceleration signal, from the time domain, in direction Z, for the subject & activity |
| timegravityaccelerationmeanx | Average mean value (in Hertz) of the gravity acceleration signal, from the time domain, in direction X, for the subject & activity |
| timegravityaccelerationmeany | Average mean value (in Hertz) of the gravity acceleration signal, from the time domain, in direction Y, for the subject & activity |
| timegravityaccelerationmeanz | Average mean value (in Hertz) of the gravity acceleration signal, from the time domain, in direction Z, for the subject & activity |
| timegravityaccelerationstandardeviationx | Average standard deviation (in Hertz) of the gravity acceleration signal, from the time domain, in direction X, for the subject & activity |
| timegravityaccelerationstandardeviationy | Average standard deviation (in Hertz) of the gravity acceleration signal, from the time domain, in direction Y, for the subject & activity |
| timegravityaccelerationstandardeviationz | Average standard deviation (in Hertz) of the gravity acceleration signal, from the time domain, in direction Z, for the subject & activity |
| timebodyaccelerationjerkmeanx | Average mean value (in Hertz) of the body acceleration jerk signal, from the time domain, in direction X, for the subject & activity |
| timebodyaccelerationjerkmeany | Average mean value (in Hertz) of the body acceleration jerk signal, from the time domain, in direction Y, for the subject & activity |
| timebodyaccelerationjerkmeanz | Average mean value (in Hertz) of the body acceleration jerk signal, from the time domain, in direction Z, for the subject & activity |
| timebodyaccelerationjerkstandardeviationx | Average standard deviation (in Hertz) of the body acceleration jerk signal, from the time domain, in direction X, for the subject & activity |
| timebodyaccelerationjerkstandardeviationy | Average standard deviation (in Hertz) of the body acceleration jerk signal, from the time domain, in direction Y, for the subject & activity |
| timebodyaccelerationjerkstandardeviationz | Average standard deviation (in Hertz) of the body acceleration jerk signal, from the time domain, in direction Z, for the subject & activity |
| timebodygyroscopemeanx | Average mean value (in Hertz) of the body gyroscope signal, from the time domain, in direction X, for the subject & activity |
| timebodygyroscopemeany | Average mean value (in Hertz) of the body gyroscope signal, from the time domain, in direction Y, for the subject & activity |
| timebodygyroscopemeanz | Average mean value (in Hertz) of the body gyroscope signal, from the time domain, in direction Z, for the subject & activity |
| timebodygyroscopestandardeviationx | Average standard deviation (in Hertz) of the body gyroscope signal, from the time domain, in direction X, for the subject & activity |
| timebodygyroscopestandardeviationy | Average standard deviation (in Hertz) of the body gyroscope signal, from the time domain, in direction Y, for the subject & activity |
| timebodygyroscopestandardeviationz | Average standard deviation (in Hertz) of the body gyroscope signal, from the time domain, in direction Z, for the subject & activity |
| timebodygyroscopejerkmeanx | Average mean value (in Hertz) of the body gyroscope jerk signal, from the time domain, in direction X, for the subject & activity |
| timebodygyroscopejerkmeany | Average mean value (in Hertz) of the body gyroscope jerk signal, from the time domain, in direction Y, for the subject & activity |
| timebodygyroscopejerkmeanz | Average mean value (in Hertz) of the body gyroscope jerk signal, from the time domain, in direction Z, for the subject & activity |
| timebodygyroscopejerkstandardeviationx | Average standard deviation (in Hertz) of the body gyroscope jerk signal, from the time domain, in direction X, for the subject & activity |
| timebodygyroscopejerkstandardeviationy | Average standard deviation (in Hertz) of the body gyroscope jerk signal, from the time domain, in direction Y, for the subject & activity |
| timebodygyroscopejerkstandardeviationz | Average standard deviation (in Hertz) of the body gyroscope jerk signal, from the time domain, in direction Z, for the subject & activity |
| timebodyaccelerationmagnitutemean | Average mean value (in Hertz) of the body acceleration signal magnitude, from the time domain, for the subject & activity |
| timebodyaccelerationmagnitutestandardeviation | Average standard deviation (in Hertz) of the body acceleration signal magnitude, from the time domain, for the subject & activity |
| timegravityaccelerationmagnitutemean | Average mean value (in Hertz) of the gravity acceleration signal magnitude, from the time domain, for the subject & activity |
| timegravityaccelerationmagnitutestandardeviation | Average standard deviation (in Hertz) of the gravity acceleration signal magnitude, from the time domain, for the subject & activity |
| timebodyaccelerationjerkmagnitutemean | Average mean value (in Hertz) of the body acceleration jerk signal magnitude, from the time domain, for the subject & activity |
| timebodyaccelerationjerkmagnitutestandardeviation | Average standard deviation (in Hertz) of the body acceleration jerk signal magnitude, from the time domain, for the subject & activity |
| timebodygyroscopemagnitutemean | Average mean value (in Hertz) of the body gyroscope signal magnitude, from the time domain, for the subject & activity |
| timebodygyroscopemagnitutestandardeviation | Average standard deviation (in Hertz) of the body gyroscope signal magnitude, from the time domain, for the subject & activity |
| timebodygyroscopejerkmagnitutemean | Average mean value (in Hertz) of the body gyroscope jerk signal magnitude, from the time domain, for the subject & activity |
| timebodygyroscopejerkmagnitutestandardeviation | Average standard deviation (in Hertz) of the body gyroscope jerk signal magnitude, from the time domain, for the subject & activity |
| frequencybodyaccelerationmeanx | Average mean value (in Hertz) of the body acceleration signal, from the frequency domain, in direction X, for the subject & activity |
| frequencybodyaccelerationmeany | Average mean value (in Hertz) of the body acceleration signal, from the frequency domain, in direction Y, for the subject & activity |
| frequencybodyaccelerationmeanz | Average mean value (in Hertz) of the body acceleration signal, from the frequency domain, in direction Z, for the subject & activity |
| frequencybodyaccelerationstandardeviationx | Average standard deviation (in Hertz) of the body acceleration signal, from the frequency domain, in direction X, for the subject & activity |
| frequencybodyaccelerationstandardeviationy | Average standard deviation (in Hertz) of the body acceleration signal, from the frequency domain, in direction Y, for the subject & activity |
| frequencybodyaccelerationstandardeviationz | Average standard deviation (in Hertz) of the body acceleration signal, from the frequency domain, in direction Z, for the subject & activity |
| frequencybodyaccelerationjerkmeanx | Average mean value (in Hertz) of the body acceleration jerk signal, from the frequency domain, in direction X, for the subject & activity |
| frequencybodyaccelerationjerkmeany | Average mean value (in Hertz) of the body acceleration jerk signal, from the frequency domain, in direction Y, for the subject & activity |
| frequencybodyaccelerationjerkmeanz | Average mean value (in Hertz) of the body acceleration jerk signal, from the frequency domain, in direction Z, for the subject & activity |
| frequencybodyaccelerationjerkstandardeviationx | Average standard deviation (in Hertz) of the body acceleration jerk signal, from the frequency domain, in direction X, for the subject & activity 

|
| frequencybodyaccelerationjerkstandardeviationy | Average standard deviation (in Hertz) of the body acceleration jerk signal, from the frequency domain, in direction Y, for the subject & activity 

|
| frequencybodyaccelerationjerkstandardeviationz | Average standard deviation (in Hertz) of the body acceleration jerk signal, from the frequency domain, in direction Z, for the subject & activity 

|
| frequencybodygyroscopemeanx | Average mean value (in Hertz) of the body gyroscope signal, from the frequency domain, in direction X, for the subject & activity |
| frequencybodygyroscopemeany | Average mean value (in Hertz) of the body gyroscope signal, from the frequency domain, in direction Y, for the subject & activity |
| frequencybodygyroscopemeanz | Average mean value (in Hertz) of the body gyroscope signal, from the frequency domain, in direction Z, for the subject & activity |
| frequencybodygyroscopestandardeviationx | Average standard deviation (in Hertz) of the body gyroscope signal, from the frequency domain, in direction X, for the subject & activity |
| frequencybodygyroscopestandardeviationy | Average standard deviation (in Hertz) of the body gyroscope signal, from the frequency domain, in direction Y, for the subject & activity |
| frequencybodygyroscopestandardeviationz | Average standard deviation (in Hertz) of the body gyroscope signal, from the frequency domain, in direction Z, for the subject & activity |
| frequencybodyaccelerationmagnitutemean | Average mean value (in Hertz) of the body acceleration signal magnitude, from the frequency domain, for the subject & activity |
| frequencybodyaccelerationmagnitutestandardeviation | Average standard deviation (in Hertz) of the body acceleration signal magnitude, from the frequency domain, for the subject & activity |
| frequencybodyaccelerationjerkmagnitutemean | Average mean value (in Hertz) of the body acceleration jerk signal magnitude, from the frequency domain, for the subject & activity |
| frequencybodyaccelerationjerkmagnitutestandardeviation | Average standard deviation (in Hertz) of the body acceleration jerk signal magnitude, from the frequency domain, for the subject & 

activity |
| frequencybodygyroscopemagnitutemean | Average mean value (in Hertz) of the body gyroscope signal magnitude, from the frequency domain, for the subject & activity |
| frequencybodygyroscopemagnitutestandardeviation | Average standard deviation (in Hertz) of the body gyroscope signal magnitude, from the frequency domain, for the subject & activity |
| frequencybodygyroscopejerkmagnitutemean | Average mean value (in Hertz) of the body gyroscope jerk signal magnitude, from the frequency domain, for the subject & activity |
| frequencybodygyroscopejerkmagnitutestandardeviation | Average standard deviation (in Hertz) of the body gyroscope jerk signal magnitude, from the frequency domain, for the subject & activity |
