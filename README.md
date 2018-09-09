### Getting and Cleaning Data - Course Project <br>
This is the course project for the Getting and Cleaning Data Coursera course. The R script, run_analysis.R, does the following:<br>

* Download the dataset if it does not already exist in the working directory<br>
* Load the activity and feature info<br>
* Loads both the training and test datasets, keeping only those columns which reflect a mean or standard deviation<br>
* Loads the activity and subject data for each dataset, and merges those columns with the dataset<br>
* Merges the two datasets<br>
* Converts the activity and subject columns into factors<br>
* Creates a tidy dataset that consists of the average (mean) value of each variable for each subject and activity pair.<br><br>

# Content<br>
* README.md, this file, which provides an overview of the data set and how it was created.
* tidy_data.txt, which contains the data set.
* CodeBook.md, the code book, which describes the contents of the data set (data, variables and transformations used to generate the data).
* run_analysis.R, the R script that was used to create the data set (see the Creating the data set section below)
