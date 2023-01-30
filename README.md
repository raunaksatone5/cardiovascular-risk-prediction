# Project Title : Cardiovascular Risk Prediction
![image](https://user-images.githubusercontent.com/102457644/204709975-ab06965d-0a1f-478b-a615-034dc97f900b.png)

## Problem Description
The dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes.

## Data Description

* Sex: male or female("M" or "F")
* Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous) Behavioral
* is_smoking: whether or not the patient is a current smoker ("YES" or "NO")
* Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.) Medical( history)
* BP Meds: whether or not the patient was on blood pressure medication (Nominal)
* Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)
* Diabetes: whether or not the patient had diabetes (Nominal) Medical (current)
* Tot Chol: total cholesterol level (Continuous)
* Sys BP: systolic blood pressure (Continuous)
* Dia BP: diastolic blood pressure (Continuous)
* BMI: Body Mass Index (Continuous)
* Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of large number of possible values.)
* Glucose: glucose level (Continuous) Predict variable (desired target)
* 10-year risk of coronary heart disease CHD(binary: “1”, means “Yes”, “0” means “No”) - DV
## Business Use Case:
* Early Risk Detection: By using cardiovascular risk prediction models, healthcare providers can identify patients who are at high risk of cardiovascular disease and take preventive measures.
* Personalized Treatment Planning: Predictive models can help healthcare providers tailor treatment plans based on a patient's individual risk profile, leading to more effective and personalized care.
* Improved Patient Outcomes: By detecting cardiovascular risk early and taking proactive measures, healthcare providers can reduce the incidence of heart disease and improve patient outcomes.
* Better Resource Allocation: Predictive models can help healthcare providers prioritize patients based on their risk level, leading to more efficient use of resources and improved patient care.
* Reduction in Healthcare Costs: By detecting and treating cardiovascular risk early, healthcare providers can reduce the cost of treatment and improve patient outcomes, leading to overall cost savings.
* Improved Public Health: By detecting cardiovascular risk early and implementing preventive measures, healthcare providers can improve public health and reduce the incidence of heart disease in the general population.

## Data Pre-Processing
* Got the descriptive information of the data.
* checked for null values if any
* Checked for Outliers and duplicated values if any.

## Data Cleaning
* Dropped the id column since it is of no significance to our model training
* Imputed null values with knn imputer and simple imputer
* treated outliers

## Feature Engineering
* applied one hot encoding to is_smoking and sex columns and converted them to binary values
* separated continuos and discrete features 
* checked corelation with heatmap and found sysBP and diaBp corelated
* created a new feature avg with the help of sysBP and diaBP

## Exploratory Data Analysis
* Checked the target variable and fount it to e imbalanced. Risk to non risk rate ratio was 1:6 approx.
* checked for the distribution of independent variables with distplot and with the hue of target variable.
* Visualized age vs sex and found out the patients above age 50 are at high risk.
* Men are more likely to have risk related to heart.

## Model training :
* Splitted data into indepdendent and dependent variable
* handled imbalanced target variable with the help of SMOTE
* Standardized resampled data using StandardScaler
* defined funvtions to train linear and non-linear models and get their performance metrics
* Performance metrics used were accuracy_score,precision_score, recall_score,f1_score
* trained models such as logistic regression, KNN, Decision trees,SVM,Random Forest and
Found Random Forest as the best model with Recall of 93%.
