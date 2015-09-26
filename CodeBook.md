# CodeBook for the Getting and Cleaning Data Course Project

Script is situated in the run_analysis.R file.

## The script defines the following algorithm

1. Determined the location of the file names of the project.
2. Created a function (Merges()) to perform data frame, created titles (labels), and added factor names (activity and subject)
3. The Merges() function (step 2) used to making and merging the data from two data sets. Aditional function rbind() is used. 
4. A "dplyr" library loaded for working with data frame. From the data frame "data" extracted columns titled "mean.." and "std..". It loaded to the "mydata" data frame. 
5. A "reshape2" library loaded for data conversion. A "melt_data" data frame with data grouped according to subject and activites (melt() finction is used) is formed.
6. An "out_data" data frame is formed (function dcast() is used). The "out_data" includes grouped by subject and activites data set. 
7. The "out_data" is written to an "out_data.txt" file (The "out_data.txt" file is situated in "directory" folder)

## Variables:

data - the merged data frame from the file "test / subject_test.txt", "test / X_test.txt", "test / y_test.txt", "train / subject_train.txt", "train / X_train.txt", "train / y_train .txt ". It takes the column names from the file" features.txt "names and the name of Activities from the file "activity_labels.txt"

mydata - the data frame with only the measurements on the mean and standard deviation for each measurement. It also includes the names of the activities and subject

melt_data - the data frame with the measurements for each activity and each subject. 

out_data - the independent tidy data set with the average of each variable for each activity and each subject
