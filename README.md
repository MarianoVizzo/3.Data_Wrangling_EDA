<div id="header" align="center">
    <img src="https://media.giphy.com/media/x7zOaeZHee5RVSVw5T/giphy.gif" width="350"/> 
    <h1 align="center"> PROJECT: DATA WRANGLING AND EXPLORATORY DATA ANALYSIS </h1>
</div>

## A. DATASET INFORMATION

### A.1. CONTEXT

- *Kavak* is a company that buys and sells used cars on the market. Its main difference from its competitors is that its used car buying process is automated on its website, allowing users to make their trades and explore options easily without leaving their home.

- The company has a historical dataset that includes information and characteristics of the cars, with a total record of 240 rows and 26 variables.

### A.2. PROJECT OBJETIVE
- **The objective of the project is to apply different techniques of cleaning, transformation and preparation of data, together with an exploratory analysis of data, obtaining a dataset suitable for later use.**

## B. ABOUT THE PROJECT DOCUMENTATION 

### B.1. HOW TO READ THE DOCUMENTATION? 

- Read the file named "Data_Wrangling_y_EDA.ipynb" where you can visualize the Python code in Google Colaboratory.
- 
- Within the Python code, you will find an organized outline with interpretations and analyses developed.
  
### B.2. DOCUMENTATION OUTLINE 

#### 1. Project Storytelling.
#### 2. Dataset Information.
#### 3. Exploratory Data Analysis (EDA).
#### 4. Data Cleaning and Transformation (Data Wrangling).
#### 5. Connection with Public Apis.
#### 6. Classification and Regression Algorithms & Clustering Algorithms I.
#### 7. Clustering Algorithms II & Algorithms Selection and Model Training I.
#### 8. Algorithm Selection and Model Training II &  Model Validation - Metrics.
#### 9. Machine Learning Models Improvement I and II.
#### 10. Training with Multiple Models.
#### 11. Boosting.
#### 12. Conclusions.

## C. LIBRARIES USED IN PYTHON 



<div id="header" align="center">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExem4zamFrZXEydjB5Znk1aXZmOHN2YzRkOXJ1aW84M2d2aTVkMWVoZCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/coxQHKASG60HrHtvkt/giphy.gif" width="300" />  
</div>

#### 1. Pandas

`import pandas as pd`

#### 2. NumPy

`import numpy as np`

#### 3. Matplotlib

`import matplotlib as mpl`
`import matplotlib.pyplot as plt`

#### 4. Seaborn

 `import seaborn as sns`

#### 5. Scikit-learn

`import sklearn as sk`
`from sklearn import model_selection`
`from sklearn import ensemble`
`from sklearn import metrics`
`from sklearn import tree`
`from sklearn.decomposition import PCA`
`rom sklearn.model_selection import train_test_split`
`from sklearn.metrics import mean_squared_error`
`from sklearn.metrics import accuracy_score`
`from sklearn.model_selection import GridSearchCV`
`from sklearn.model_selection import RandomizedSearchCV`
`from sklearn.experimental import enable_halving_search_cv`
`from sklearn.model_selection import HalvingGridSearchCV`
`from sklearn.model_selection import HalvingRandomSearchCV`
`from sklearn.preprocessing import LabelEncoder`
`from sklearn.metrics import accuracy_score, classification_report`
`from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier`
`from sklearn.tree import DecisionTreeClassifier`
`from sklearn.linear_model import LogisticRegression`
`from sklearn.svm import SVC`
`from sklearn.ensemble import VotingClassifier`
`from sklearn.model_selection import GridSearchCV`
`from sklearn.feature_selection import SelectFromModel`
`from sklearn.ensemble import StackingClassifier, BaggingClassifier, AdaBoostClassifier, VotingClassifier`
`from sklearn.metrics import recall_score, precision_score, accuracy_score`
`from sklearn.model_selection import LeaveOneOut, cross_val_score`

#### 6. XGBoost

`import xgboost as xgb`


## D. ABOUT THE PROJECT

- This project was developed as part of my *Data Scientist* career at *Coderhouse* as the *Final Project*.


DATA WRANGLING Y EDA
1. INTRODUCCIÓN
El siguiente notebook se desarrollará una rutina de preprocesamiento sobre un conjunto de datos.

1) En primer lugar, se obtiene una breve descripción estadística y gráfica de cada una de las variables.

2) En segundo lugar, se aplicarán técnicas de limpieza, transformación y preparación de conjuntos de datos para su análisis.

3) En tercer lugar, se realizará un Análisis Exploratorio de Datos (EDA) luego de aplicar las técnicas de limpieza de datos.

2. PREPARACIÓN DE DATOS EN EL CONJUNTO DE DATOS


price                float64
dtype: object
