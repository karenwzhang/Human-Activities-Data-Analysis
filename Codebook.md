The Run_analysis.R files performs data preparation and the following 5 steps to clean the data.
    1. DOwnload zip file and upzip file 
    2. Merge training and test sets to create one data set
       features<-features.txt
       activities<- activity_labels.txt
       subject_test <- subject_test.txt
       x_test <- X_test.txt
       y_test <- y_test.txt
       subject_train <- subject_train.txt
       x_train <- X_train.txt
       y_train <- y_train.txt
       
       merge x_train and x_test files to create x file
       merge y_train and y_test files to create y file
       merge subject_train and subject_test files to create subject file
       merge the above created x,y and subject files to create Merged_Data files
       
    3.Extracts only the measurements on the mean and standard deviation for each measurement.
      TidyData is created by subsetting Merged_Data files, only selecting columns subject, code, and columns that            contains mean or std.
    
    4.Uses descriptive activity names to name the activities in the data set
      Entire numbers in code column of the TidyData replaced with corresponding activity taken from second column of         the activities variable.
      
    5.Appropriately labels the data set with descriptive variable names. 
      All Acc in column’s name replaced by Accelerometer
      All Gyro in column’s name replaced by Gyroscope
      All BodyBody in column’s name replaced by Body
      All Mag in column’s name replaced by Magnitude
      All start with character f in column’s name replaced by Frequency
      All start with character t in column’s name replaced by Time
    
    6. From the data set in step 5, creates a second, independent tidy data set with the average of each variable for         each activity and each subject.
      FinalResult.txt file is created. 