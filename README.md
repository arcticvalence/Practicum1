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
* Created multiple variables with different conditions to test feature selection and model performance


## Libraries Used
library(stringr), (naniar), (caret), (dummies), (glmnet), (fastDummies), (varhandle), (ggplot2), (cowplot), (corrplot), (ISLR), (earth), (party), (keep), (tidyverse), (car), (dplyr), (ROCR), (GGally), (ggdendro), (rpart), (rpart.plot), (e1071)

## Modeling Techniques
Logistic Regression was used in this project as the data is all categorical. A combination of gbmImp, the marsModel and glm were utilized for feature selection. I additionally explored the Naieve Bayes method and a Decision Tree model but added the decision tree to my next steps of this project were I to take one.

## Analysis Methods
For the analysis, I utilized tabled confision matrix to show the number of accurately vs. inaccurately predicted categories. I also utilized a precision/recall graph for each model, I also utilized the precision, recall, f1 score and specificity to access all 3 versions of the model I showcased in my presentation.

![alt text](https://user-images.githubusercontent.com/50388830/123482297-3d139f80-d5c2-11eb-8c09-f3298081b168.png)

![alt text](https://user-images.githubusercontent.com/50388830/123482298-3d139f80-d5c2-11eb-962b-e20addbc850c.png)
![alt text](https://user-images.githubusercontent.com/50388830/123482299-3dac3600-d5c2-11eb-84c5-6b33bd1289ee.png)
![alt text](https://user-images.githubusercontent.com/50388830/123482302-3e44cc80-d5c2-11eb-90ee-1332602d1e69.png)
![alt text](https://user-images.githubusercontent.com/50388830/123482304-3e44cc80-d5c2-11eb-85ab-ddd2753701b7.png)
![alt text](https://user-images.githubusercontent.com/50388830/123482306-3e44cc80-d5c2-11eb-97e9-79cabfedcf6b.png)


## References
Forte, R. M. (2015). Mastering predictive analytics with R. Packt Publishing Ltd.
https://mgimond.github.io/Stats-in-R/Logistic.html

  
  
  
  
  
  
  
  
A classifiation model to predict a desire to return to the office based on external factors
  
Project for Regis University MSDS692, Data Science Practicum I
  
Erin Tansley - holco811@regis.edu
Documentation and Storage for ET Practicum 1
  
Project Files:
  
returntowork5102021.csv - Raw data self collected that may be used without license issues
  
  
