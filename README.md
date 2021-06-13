# Predicting Return To The Office


## Project Summary
This project was created using a self-collected dataset via a Google Docs form. The main objective of my analysis was to answer the question: "Can you predict if office workers will want to return to the office after the COVID pandemic has subsided based on external factors?". The modeling I chose for this project was logistic regression in R utilizing R Studio. 

## Data Cleaning Methods
This project required several things be changed in order to begin using the machine learning model:
* Updated column headers for clarity and ease
* Removed the timestamp column that Google automatically assigned as key values for each row
* Removed the UserID column as it was only relevant for the survey payment information
* Removed specific rows that were answered by individuals who did not reside in the United States
* Stripped extra characters out of the ZipCode column
* Updated data that upon export saved to "5-Mar" instead of the category of 3-5
* Updated various versions of "N/A" to be uniform and replaced with 0
* Updated LifeGoal and Hobby category names for clarity and ease
* Converted all columns to factors
* Converted the ReturnToOffice column as binary for performance testing


## Libraries Used
library(stringr), (naniar), (caret), (dummies)
library(glmnet)
library(fastDummies)
library(varhandle)
library(ggplot2)
library(cowplot)
library(corrplot)
library(ISLR)
library(earth)

## Modeling Techniques
Logistic Regression was used in this project as the data is all categorical. A combination of gbmImp, the marsModel and glm were utilized for feature selection.

  A classifiation model to predict a desire to return to the office based on external factors
  
  Project for Regis University MSDS692, Data Science Practicum I
  
  Erin Tansley
  
  holco811@regis.edu
  Documentation and Storage for ET Practicum 1
  
  Project Files:
  
  returntowork5102021.csv - Raw data self collected that may be used without license issues
  
  
