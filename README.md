# Getting-and-Cleaning-Data

This is the github repository for the **getting and cleaning data** coursera project by John Hopkins

**Project Description**

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 
1) a tidy data set as described below
2) a link to a Github repository with your script for performing the analysis, and
3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md.

**Data Description**

The data considered for the Project represent data collected from the accelerometers from the Samsung Galaxy S smartphone.

A full description is available at the web site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones.

The whole data package can be downloaded at the following link: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

**Data Analysis**

To perform the data analysis it is required to perform the following steps:

Clone this repository into a folder on the local machine: git clone https://github.com/leriomaggio/getting-and-cleaning-data.git

Set the Working Directory to the folder where the Git repository has been cloned:

 setwd("<CLONE REPO FOLDER PATH>")
Download and Unzip the data package by clicking at the following url: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip or by sourcing the downloadata.R w/ the command:

 source("./downloadata.R")
This R script will download the data package, and it will store the downloaded package into a dataset.zip file located into the datasets folder.

Source the run_analysis.R script:

  source("run_analysis.R")
Sourcing the run_analysis.R script will perform the actual analysis. In particular:

Read the Dataset
Merges the training and the test sets to create one single data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
After performing the analysis, the following files will be created:

merged_and_cleaned_dataset.txt (corresponding to a 10299x68 data frame)
tidy_dataset_with_average_values.txt (corresponding to a 180x68 data frame)
Use data: to read and use the data it is necessary to run the following command:

  data <- read.table("tidy_dataset_with_average_values.txt")
It will correspond to a 180x68 data frame w/ 30 subjects and 6 activities (i.e., 30 x 6 = 180 rows)

 **End**
The provided R script makes assumptions on the location of files to process (dataset). However, no assumptions is made on the numbers of rows and columns of the data frame to process during the analysis steps.
