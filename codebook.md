---
title: "Codebook"
author: "aponici"
date: "February 18, 2016"
output: html_document
---

Information
------------------------

For each record in the dataset it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope.
- Its activity label.

run_analysis.R
-----------------

1. Checks to see if UCI Har Dataset directory exists and creates it if it does not.
2. It downloads the **UCI HAR Dataset** data set and puts the zip file in the working directrory. After it is downloaded, it unzips the file into the UCI HAR Dataset folder. 
3. It loads the **train** and **test** data sets and appends the two datasets into one data frame. This is done using `rbind`.
4. It extracts just the *mean* and *standard deviation* from the **features** data set. This is done using `grep`.
5. After cleaning the column names, these are applied to the **x** data frame.  
6. After loading **activities** data set, it converts it to lower case using `tolower` and removes underscore using `gsub`. *activity* and *subject* column names are named for **y** and **subj** data sets, respectively.
7. The three data sets, **x**, **y** and **subj**, are merged. Then, it is exported as a *txt* file into the Project folder in the same working directory, named **merged&labeled.txt**.
8. The *mean* of activities and subjects are created into a separate tidy data set which is exported into the Project folder as *txt* file; this is named **averageOfEachVariable&Subject.txt**.

### Variable Descriptions


| Variable | Description
-----------|-------------
| activities | The activity performed
| subject | Subject ID
| tbodyacc-mean-x | Mean time for acceleration of body for X direction
| tbodyacc-mean-y | Mean time for acceleration of body for Y direction
| tbodyacc-mean-z | Mean time for acceleration of body for Z direction
| tbodyacc-std-x | Standard deviation of time for acceleration of body for X direction
| tbodyacc-std-y | Standard deviation of time for acceleration of body for Y direction
| tbodyacc-std-z | Standard deviation of time for acceleration of body for Z direction
| tgravityacc-mean-x | Mean time of acceleration of gravity for X direction
| tgravityacc-mean-y | Mean time of acceleration of gravity for Y direction
| tgravityacc-mean-z | Mean time of acceleration of gravity for Z direction
| tgravityacc-std-x | Standard deviation of time of acceleration of gravity for X direction
| tgravityacc-std-y | Standard deviation of time of acceleration of gravity for Y direction
| tgravityacc-std-z | Standard deviation of time of acceleration of gravity for Z direction
| tbodyaccjerk-mean-x | Mean time of body acceleration jerk for X direction
| tbodyaccjerk-mean-y | Mean time of body acceleration jerk for Y direction
| tbodyaccjerk-mean-z | Mean time of body acceleration jerk for Z direction
| tbodyaccjerk-std-x | Standard deviation of time of body acceleration jerk for X direction
| tbodyaccjerk-std-y | Standard deviation of time of body acceleration jerk for Y direction
| tbodyaccjerk-std-z | Standard deviation of time of body acceleration jerk for Z direction
| tbodygyro-mean-x | Mean body gyroscope measurement for X direction
| tbodygyro-mean-y | Mean body gyroscope measurement for Y direction
| tbodygyro-mean-z | Mean body gyroscope measurement for Z direction
| tbodygyro-std-x | Standard deviation of body gyroscope measurement for X direction
| tbodygyro-std-y | Standard deviation of body gyroscope measurement for Y direction
| tbodygyro-std-z | Standard deviation of body gyroscope measurement for Z direction
| tbodygyrojerk-mean-x | Mean jerk signal of body for X direction
| tbodygyrojerk-mean-y | Mean jerk signal of body for Y direction
| tbodygyrojerk-mean-z | Mean jerk signal of body for Z direction
| tbodygyrojerk-std-x | Standard deviation of jerk signal of body for X direction
| tbodygyrojerk-std-y | Standard deviation of jerk signal of body for Y direction
| tbodygyrojerk-std-z | Standard deviation of jerk signal of body for Z direction
| tbodyaccmag-mean | Mean magnitude of body Acc
| tbodyaccmag-std | Standard deviation of magnitude of body Acc
| tgravityaccmag-mean | Mean gravity acceleration magnitude
| tgravityaccmag-std | Standard deviation of gravity acceleration magnitude
| tbodyaccjerkmag-mean | Mean magnitude of body acceleration jerk
| tbodyaccjerkmag-std | Standard deviation of magnitude of body acceleration jerk
| tbodygyromag-mean | Mean magnitude of body gyroscope measurement
| tbodygyromag-std | Standard deviation of magnitude of body gyroscope measurement
| tbodygyrojerkmag-mean | Mean magnitude of body body gyroscope jerk measurement
| tbodygyrojerkmag-std | Standard deviation of magnitude of body body gyroscope jerk measurement
| fbodyacc-mean-x | Mean frequency of body acceleration for X direction
| fbodyacc-mean-y | Mean frequency of body acceleration for Y direction
| fbodyacc-mean-z | Mean frequency of body acceleration for Z direction
| fbodyacc-std-x | Standard deviation of frequency of body acceleration for X direction
| fbodyacc-std-y | Standard deviation of frequency of body acceleration for Y direction
| fbodyacc-std-z | Standard deviation of frequency of body acceleration for Z direction
| fbodyaccjerk-mean-x | Mean frequency of body accerlation jerk for X direction
| fbodyaccjerk-mean-y | Mean frequency of body accerlation jerk for Y direction
| fbodyaccjerk-mean-z | Mean frequency of body accerlation jerk for Z direction
| fbodyaccjerk-std-x | Standard deviation frequency of body accerlation jerk for X direction
| fbodyaccjerk-std-y | Standard deviation frequency of body accerlation jerk for Y direction
| fbodyaccjerk-std-z | Standard deviation frequency of body accerlation jerk for Z direction
| fbodygyro-mean-x | Mean frequency of body gyroscope measurement for X direction
| fbodygyro-mean-y | Mean frequency of body gyroscope measurement for Y direction
| fbodygyro-mean-z | Mean frequency of body gyroscope measurement for Z direction
| fbodygyro-std-x | Standard deviation frequency of body gyroscope measurement for X direction
| fbodygyro-std-y | Standard deviation frequency of body gyroscope measurement for Y direction
| fbodygyro-std-z | Standard deviation frequency of body gyroscope measurement for Z direction
| fbodyaccmag-mean | Mean frequency of body acceleration magnitude
| fbodyaccmag-std | Standard deviation of frequency of body acceleration magnitude
| fbodybodyaccjerkmag-mean | Mean frequency of body acceleration jerk magnitude
| fbodybodyaccjerkmag-std | Standard deviation of frequency of body acceleration jerk magnitude
| fbodybodygyromag-mean | Mean frequency of magnitude of body gyroscope measurement
| fbodybodygyromag-std | Standard deviation of frequency of magnitude of body gyroscope measurement
| fbodybodygyrojerkmag-mean | Mean frequency of magnitude of body gyroscope jerk measurement
| fbodybodygyrojerkmag-std | Standard deviation frequency of magnitude of body gyroscope jerk measurement