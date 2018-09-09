# Code Book

This code book describes the variables, the data, and any transformations or work performed to clean up the data.

## Source of the Data:

* Source of the original data:
  [https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip]().
* Original description:
  [http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones]().

## Dataset Information ##

**Human Activity Recognition Using Smartphones Dataset**

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. 
Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) 
wearing a smartphone (Samsung Galaxy S II) on the waist.

## Data Manipulation details

The `run_analysis.R` script performs the following operations to clean and transform the data:
     0. Read the dataset
     1. Merges the training and the test sets to create one single data set.
     2. Extracts only the measurements on the mean and standard deviation for each measurement. 
     3. Uses descriptive activity names to name the activities in the data set
     4. Appropriately labels the data set with descriptive variable names. 
     5. Creates a second, independent tidy data set with the average of each variable 
         for each activity and each subject.


### Extracts only the measurements on the mean and standard deviation for each measurement. 

This results in a `10299 x 66` data frame, where `66` out of `561` features are selected and filtered in this step.
All measurements correspond to `numeric` (real) numbers in the range `(-1, 1)`.

### Uses descriptive activity names to name the activities in the data set ###

- WALKING
- WALKING_UPSTAIRS
- WALKING_DOWNSTAIRS
- SITTING
- STANDING
- LAYING

### Appropriately labels the data set with descriptive variable names. ###

The script properly labels the dataset with descriptive names:
all feature names and activity names are converted to ,
underscores and brackets ("(", ")") are removed.

Finally, all the data are merged into a single `10299x68` data frame corresponding to:

- `10299x1` data frame of `subject IDs`;
- `10299x1` data frame of `activity labels`;
- `10299x68` data frame of `features`.

Subject IDs are `integers` with values in range `[1, 30]`.

Names of the attributes corresponds to:

- "tbodyacc-mean-x" 
- "tbodyacc-mean-y" 
- "tbodyacc-mean-z" 
- "tbodyacc-std-x" 
- "tbodyacc-std-y" 
- "tbodyacc-std-z" 
- "tgravityacc-mean-x" 
- "tgravityacc-mean-y" 
- "tgravityacc-mean-z" 
- "tgravityacc-std-x" 
- "tgravityacc-std-y" 
- "tgravityacc-std-z" 
- "tbodyaccjerk-mean-x" 
- "tbodyaccjerk-mean-y" 
- "tbodyaccjerk-mean-z" 
- "tbodyaccjerk-std-x" 
- "tbodyaccjerk-std-y" 
- "tbodyaccjerk-std-z" 
- "tbodygyro-mean-x" 
- "tbodygyro-mean-y" 
- "tbodygyro-mean-z"
- "tbodygyro-std-y"
- "tbodygyro-std-z"
- "tbodygyrojerk-mean-x"
- "tbodygyrojerk-mean-y"
- "tbodygyrojerk-mean-z"
- "tbodygyrojerk-std-x"
- "tbodygyrojerk-std-y"
- "tbodygyrojerk-std-z"
- "tbodyaccmag-mean"
- "tbodyaccmag-std"
- "tgravityaccmag-mean"
- "tgravityaccmag-std"
- "tbodyaccjerkmag-mean"
- "tbodyaccjerkmag-std"
- "tbodygyromag-mean"
- "tbodygyromag-std"
- "tbodygyrojerkmag-mean"
- "tbodygyrojerkmag-std"
- "fbodyacc-mean-x"
- "fbodyacc-mean-y"
- "fbodyacc-mean-z"
- "fbodyacc-std-x"
- "fbodyacc-std-y"
- "fbodyacc-std-z"
- "fbodyaccjerk-mean-x"
- "fbodyaccjerk-mean-y"
- "fbodyaccjerk-mean-z"
- "fbodyaccjerk-std-x"
- "fbodyaccjerk-std-y"
- "fbodyaccjerk-std-z"
- "fbodygyro-mean-x"
- "fbodygyro-mean-y"
- "fbodygyro-mean-z"
- "fbodygyro-std-x"
- "fbodygyro-std-y"
- "fbodygyro-std-z"
- "fbodyaccmag-mean"
- "fbodyaccmag-std"
- "fbodybodyaccjerkmag-mean"
- "fbodybodyaccjerkmag-std"
- "fbodybodygyromag-mean"
- "fbodybodygyromag-std"
- "fbodybodygyrojerkmag-mean"
- "fbodybodygyrojerkmag-std"




