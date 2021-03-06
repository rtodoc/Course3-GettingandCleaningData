# Data Description

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.  See the full description of the data at the site below.[1][2]

# Steps to Clean

1.	Data should first be downloaded from this link:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

2.	The relevant files are then automatically loaded into R when the script is run.  They are:
*	features.txt: List of all variables that correspond to the columns in the training and test sets
*	activity_labels.txt: Identifies the corresponding name of the numerical activities found in y_train.txt and y_test.txt
*	X_train.txt: Training set
*	y_train.txt: Training activity labels
*	subject_train.txt: Each row identifies the subject who performed the activity for each corresponding line of the training set
*	X_test.txt: Test set
*	y_test.txt: Test activity labels
*	subject_test.txt: Each row identifies the subject who performed the activity for each row in the test set
 
3.	Combine the training and the test sets as well as their subject and activity labels.  This leads to one data frame which has 10299 rows of 563 variables.
4.	Find the columns that contain the mean and standard deviation and keep only these measurements.  This left us with 66 variables.  
5.	Use descriptive names for the activities by substituting the numbers for the strings found in activity_labels.txt. 
6.	Then, the variable names are cleaned up further.
7.	Lastly, the script creates a second, independent tidy data set with the average of each variable for each activity and each subject.  This file contains 180 rows of 66 variables as specified below:
   


[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
[2] http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

