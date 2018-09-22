<b> Getting-and-cleaning-data </b><br/>
<b>Course project from Coursera </b>
date: "September 14, 2018"
  
This project is to prepare a tidy data set for later analysis from the experiment data available at-https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip.<br/> 
The main procedure is as following:<br/>
    Merges the training and the test sets to create one data set.<br/>
    Extracts only the measurements on the mean and standard deviation for each measurement. <br/>
    Uses descriptive activity names to name the activities in the data set.<br/>
    Appropriately labels the data set with descriptive variable names.<br/>
    From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.<br/>

Here is how my script implements: <br/>

   1. Clean current workspace. Set up the working directory. <br/>
   2. Download the data set to working directory from the target URL. Unzip the file. <br/>
   3. Load the activity labels and features. Select the features including mean and standard deviation and assign the values to “features_need”. <br/>
   4. Load the data for test and train including subject, activity and experiment result. Select columns matching “features_need”.<br/>
   5. Combine the subject, activity and experiment result for test and train respectively and get the data sets “train” and “test”.<br/>
   6. Merge “train” and “test” to get “mergeddata”.<br/>
   7. Clean the special characters in “features_need”. Rename column names in “mergeddata” using “features_need”.<br/>
   8. Use descriptive activity names to name the activity column in “mergeddata”<br/>
   9. Take the average of each variable in “mergeddata” for each activity and each subject. Assign the value to a new data set “result”. Write the output.<br/>
