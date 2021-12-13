## Heart Disease Prediction

<p align="center">
  <img src="https://media.giphy.com/media/DhQbe54TB2Bzi/giphy.gif" alt="animated" width="300" height="200" />
</p>

[gif source](https://giphy.com)

## Table of CONTENTS 
---------------------
 * [Introduction](#intro)
 * [Aim](#aim)
 * [Dataset used](#data)
 * [Exploring the Data](#viz)
   - [Matplotlib](#matplotlib)
   - [Seaborn](#seaborn)
 * [using various model for prediction](#models)
 * [Conclusion](#conclusion)
 
 
 ## INTRODUCTION:<a name="intro"></a>
 
Heart disease describes a range of conditions that affect your heart. Diseases under the heart disease umbrella include blood vessel diseases, such as coronary artery disease, heart rhythm problems (arrhythmias) and heart defects you’re born with (congenital heart defects), among others.

The term “heart disease” is often used interchangeably with the term “cardiovascular disease”. Cardiovascular disease generally refers to conditions that involve narrowed or blocked blood vessels that can lead to a heart attack, chest pain (angina) or stroke. Other heart conditions, such as those that affect your heart’s muscle, valves or rhythm, also are considered forms of heart disease.

Heart disease is one of the biggest causes of morbidity and mortality among the population of the world. Prediction of cardiovascular disease is regarded as one of the most important subjects in the section of clinical data analysis. The amount of data in the healthcare industry is huge. Data mining turns the large collection of raw healthcare data into information that can help to make informed decisions and predictions.

According to a news article, heart disease proves to be the leading cause of death for both women and men. The article states the following :

`About 610,000 people die of heart disease in the United States every year–that’s 1 in every 4 deaths.`

`Heart disease is the leading cause of death for both men and women. More than half of the deaths due to heart disease in 2009 were in men.`

`Coronary Heart Disease(CHD) is the most common type of heart disease, killing over 370,000 people annually.`

`Every year about 735,000 Americans have a heart attack. Of these, 525,000 are a first heart attack and 210,000 happen in people who have already had a heart attack.`

This makes heart disease a major concern to be dealt with. But it is difficult to identify heart disease because of several contributory risk factors such as diabetes, high blood pressure, high cholesterol, abnormal pulse rate, and many other factors. Due to such constraints, scientists have turned towards modern approaches like Data Mining and Machine Learning for predicting the disease.

Machine learning (ML) proves to be effective in assisting in making decisions and predictions from the large quantity of data produced by the healthcare industry.
In this dataset, I will be applying Machine Learning approaches(and eventually comparing them) for classifying whether a person is suffering from heart disease or not

## AIM:<a name="aim"></a>

The goal is to check the presence of heart disease in the patient. It is integer (0 for no presence, 1 for presence).

## Dataset Used:<a name="data"></a>

This database contains 14 physical attributes based on physical testing of a patient. Blood samples are taken and the patient also conducts a brief exercise test.  In general, to confirm 100% if a patient has heart disease can be quite an invasive process, so if we can create a model that accurately predicts the likelihood of heart disease, we can help avoid expensive and invasive procedures.

Attribute Information:

`sex : 1 = Male , 0=Female`

`cp : Chest Pain`

`Angina: Angina is caused when there is not enough oxygen-rich blood flowing to a certain part of the heart. The arteries of the heart become narrow due to fatty deposits in the artery walls. The narrowing of arteries means that blood supply to the heart is reduced, causing angina`

`Value 1: typical angina || Value 2: atypical angina || Value 3: non-anginal pain || 4: asymptomatic`

`threstbps :Resting blood pressure ( Normal pressure with no exercise )`

`chol: serum cholestoral in mg/dl`
`Cholesterol means the blockage for blood supply in the blood vessels`

`fbs: fasting blood sugar > 120 mg/dl`
`(1 = true; 0 = false) blood sugar taken after a long gap between a meal and the test. Typically, it's taken before any meal in the morning.`

`restecg: resting electrocardiographic results (values 0,1,2)`
`ECG values taken while person is on rest which means no exercise and normal functioning of heart is happening`

`oldpeak = ST depression induced by exercise relative to rest`
`ST Depression is the difference between value of ECG at rest and after exercise. An electrocardiogram records the electrical signals in your heart. It's a common and painless test used to quickly detect heart problems and monitor your heart's health. Electrocardiograms — also called ECGs or EKGs — are often done in a doctor's office, a clinic or a hospital room. ECG machines are standard equipment in operating rooms and ambulances. Some personal devices, such as smart watches`

`slope: the slope of the peak exercise ST segment`
`Value 1: upsloping — Value 2: flat — Value 3: downsloping`

`ca: number of major vessels (0-3) colored by flourosopy`
`Fluoroscopy is an imaging technique that uses X-rays to obtain real-time moving images of the interior of an object. In its primary application of medical imaging, a fluoroscope (/ˈflʊərəskoʊp/) allows a physician to see the internal structure and function of a patient, so that the pumping action of the heart or the motion of swallowing, for example, can be watched`

`thal:The Types of thalassemia`
`(3 = normal; 6 = fixed defect; 7 = reversable defect)`

*Original Source: https://archive.ics.uci.edu/ml/datasets/Heart+Disease*

Creators:

Hungarian Institute of Cardiology. Budapest: Andras Janosi, M.D. University Hospital, Zurich, Switzerland: William Steinbrunn, M.D. University Hospital, Basel, Switzerland: Matthias Pfisterer, M.D. V.A. Medical Center, Long Beach and Cleveland Clinic Foundation: Robert Detrano, M.D., Ph.D.


## Exploring the Data:<a name="viz"></a>

Here I had used pandas and seaborn visualization skills.

**Matplotlib:**<a name="matplotlib"></a>
--------
Matplotlib is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms. Matplotlib can be used in Python scripts, the Python and IPython shells, the Jupyter notebook, web application servers, and four graphical user interface toolkits.You can draw up all sorts of charts(such as Bar Graph, Pie Chart, Box Plot, Histogram. Subplots ,Scatter Plot and many more) and visualization using matplotlib.

Environment Setup==
If you have Python and Anaconda installed on your computer, you can use any of the methods below to install matplotlib:

    pip: pip install matplotlib

    anaconda: conda install matplotlib
    
    import matplotlib.pyplot as plt

![matplotlib](https://eli.thegreenplace.net/images/2016/animline.gif)

for more information you can refer to [matplotlib](https://matplotlib.org/) official site

**Seaborn:**<a name="seaborn"></a>
------
Seaborn is built on top of Python’s core visualization library Matplotlib. Seaborn comes with some very important features that make it easy to use. Some of these features are:

**Visualizing univariate and bivariate data.**

**Fitting and visualizing linear regression models.**

**Plotting statistical time series data.**

**Seaborn works well with NumPy and Pandas data structures**

**Built-in themes for styling Matplotlib graphics**

**The knowledge of Matplotlib is recommended to tweak Seaborn’s default plots.**

Environment Setup==
If you have Python and Anaconda installed on your computer, you can use any of the methods below to install seaborn:

    pip: pip install seaborn

    anaconda: conda install seaborn
    
    import seaborn as sns
    
![seaborn](https://i.stack.imgur.com/uzyHd.gif)

for more information you can refer to [seaborn](https://seaborn.pydata.org/) official site.

## Data Exploration

The goal here is to gain more information from the data:

• What are you trying to solve ?

• What kind of data we have and how to treat different types ?

• What is missing from the data and how to deal with it ?

• Where are the outliers and why should you care about them?

• How can you add, change or remove features to get more out of your data ?

![download](https://user-images.githubusercontent.com/86251750/145763845-579efe15-c839-4a71-9d9b-9f6fc671159d.png)

![download](https://user-images.githubusercontent.com/86251750/145764076-f7fd756d-fd22-4f92-817f-aceef72bb89b.png)

![download](https://user-images.githubusercontent.com/86251750/145764211-c6905b1c-e2c9-4a32-9a61-62c583ddbea0.png)

**feature importance**

![download](https://user-images.githubusercontent.com/86251750/145764442-b0380898-2e2d-4831-ba66-577af81c367b.png)

**correlation of various features with target variable**

![download](https://user-images.githubusercontent.com/86251750/145764318-a5480e23-81f1-46a5-b541-3580086ff8ac.png)


## Prediction with various Models:<a name="models"></a>

I have used various classification models for the prediction to check whether the person has heart disease or not

**logistic regression**

                precision    recall  f1-score   support

           0       0.85      0.81      0.83        27
           1       0.86      0.88      0.87        34

    accuracy                           0.85        61   
    
![download](https://user-images.githubusercontent.com/86251750/145766469-5a3cd2d8-bafe-402e-9b0c-dd892276ef7f.png)
    
**support vector classifier**

                precision    recall  f1-score   support

           0       0.71      0.56      0.63        27
           1       0.70      0.82      0.76        34

    accuracy                           0.70        61

![download](https://user-images.githubusercontent.com/86251750/145765384-9cb39bac-9d51-4b93-a481-c15dcbe72e66.png)


**Naive Byes**

                precision    recall  f1-score   support

           0       0.88      0.78      0.82        27
           1       0.84      0.91      0.87        34

    accuracy                           0.85        61

![download](https://user-images.githubusercontent.com/86251750/145765534-03f500e0-2d76-4613-9eb4-2e0744746dc8.png)

**RandomForest classifier**

                precision    recall  f1-score   support

           0       0.92      0.85      0.88        27
           1       0.89      0.94      0.91        34

    accuracy                           0.90        61
    
![download](https://user-images.githubusercontent.com/86251750/145765758-c5835e9f-d46d-4f2a-9e5d-4a26e50a2052.png)

**RandomForest classifier with grid search**

                precision    recall  f1-score   support

           0       0.86      0.89      0.87        27
           1       0.91      0.88      0.90        34

    accuracy                           0.89        61
    
![download](https://user-images.githubusercontent.com/86251750/145766030-7b129390-01c8-42c5-b7b9-426147f734f3.png)
    
**DecisionTree classifier**

                precision    recall  f1-score   support

           0       0.79      0.85      0.82        27
           1       0.88      0.82      0.85        34

    accuracy                           0.84        61

![download](https://user-images.githubusercontent.com/86251750/145766162-538244be-9f01-49f9-9c6b-02559b662c79.png)

**KNN**

      Accuracy score : 68.85
      
![download](https://user-images.githubusercontent.com/86251750/145766694-2f6e2548-6687-425c-a403-0e17b9472620.png)

**XGBOOST**

                precision    recall  f1-score   support

           0       0.81      0.78      0.79        27
           1       0.83      0.85      0.84        34

    accuracy                           0.82        61
    
![download](https://user-images.githubusercontent.com/86251750/145770976-c1c07d7f-c183-4707-9e66-91b8c83cbc7d.png)


## CONCLUSION:<a name="conclusion"></a>

* The accuracy score achieved using Logistic Regression is: 85.25 %

* The accuracy score achieved using KNN CLF is: 68.85 %

* The accuracy score achieved using Support Vector Machine is: 70.49 %

* The accuracy score achieved using Gaussian Navie Bayes is: 85.25 %

* The accuracy score achieved using Random Forest with GridSearch is: 88.52 %

* The accuracy score achieved using Random Forest is: 90.16 %

* The accuracy score achieved using XGBoost is: 81.97 %

* The accuracy score achieved using Decision Tree is: 83.61 %

**From all above model we can see that RandomForest classifier gives us best result so I have used it as my final model**

***language used***
--------------------------
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

**Tools**
-----------------------
[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)    ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)   ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)  ![Made with matplotlib](https://user-images.githubusercontent.com/86251750/132984208-76ce70c7-816d-4f72-9c9f-90073a70310f.png)  ![seaborn](https://user-images.githubusercontent.com/86251750/132984253-32c04192-989f-4ebd-8c46-8ad1a194a492.png)

