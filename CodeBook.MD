Getting and Cleaning Data Project

Summer Vaught

Description:
You can get information about the variables, data, etc. in the coursera course Getting and Cleaning Data through John Hopkins University.

Source Data

The data can be found at the UCI Machind Learning Repository. The link for the data is: 
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Data Set Information

The experriments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed 6 activities
(WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy SII) on the waist. Using its 
embedded accelorometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The
experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70%
of the volunteers were selected for generating training data and the remaining 30% generated the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows
of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which as gravitation and body motion components, were 
separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low 
frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

Attribute Information:

For eacch record in the dataset it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the extimated body acceleration.
- Triaxial angular velocity from the gyroscope.
- A 561 - feature vector with time and frequency domain variables
- It's activity label.
- An identifier of the subject who carried out the  experiment.

Section 1 - Merge the training and test sets to create one data set.
I set my working directory to contain the unzipped folder contating the files, and read each file into tables:
- features.txt
- activity_labels.txt
- subject_train.txt
- x_train.txt
- y_train.txt
- subject_test.txt
- x_test.txt
- y_test.txt

Assign column names the features file and merge to create one data set.

Section 2- Extract only the measurements on the mean and standard deviation for each measurement

Create a logical vector that contains TRUE values for the ID, mean and std dev columns, and FALSE values 
for the others. Subset this data to only keep the mean and standard devation columns.

Section 3 - Use descriptive activity names to name the activities in the data set

Merge data subset with the activtyType table to include the descriptive activity names (WALKING, LAYING, etc)

Section 4 - Appropriately label the data set with descriptive activity names

use gsub function to repace and clean up the data labels.

Section 5 - Create a second, independent, tidy data set with the average of each variable for eacha ctivity and each subject.

Per the project instructions, we need to produce only a data set with the average of each variable for each activity and subject.
