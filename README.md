# Microsoft Kaggle Competition: *Malware Prediction*

This notebook is my report for [Microsoft's Kaggle competition][competition].


[competition]: https://www.kaggle.com/c/microsoft-malware-prediction



## Description

In this competition, the goal is to predict if a machine will soon be hit with malware. Microsoft wish to develop techniques to predict malware occurrences. They expect that we can help protect more than one billion machines from damage before malware happens. 



## Data
There are two dataset. one is train and the other is test. We have to predict a Windows machine’s probability of getting infected by various families of malware, based on different properties of that machine. To do this, Microsoft give us data containing these properties and the machine infections and the data are collected by Microsoft's Windows Defender.


## Problems of Microsoft Malware Prediction 

#### 1. Building time independent model  
The data is timeseries data. The train data are mostly form August and Septemer 2018 while the test are mostly from October and November 2018. As they have different timestamp, my goal is to bulid a time independent model.

#### 2. Dealing with categorical features
There are more than 90% of categorical features in data. I dealt with these features using various encoding method as shown below. 

   * Binary Encode 
   * Numeric Encode
   * Frequency Encode
   * Category Encode
   * Target Encode

#### 3. Large dataset
The size of this data is very large (train: 4.08GB, test: 3.53GB). So I need to manage memory efficiently.



## Requirements

To replicate the findings and execute the code in this notebook you will need basically the next Python packages and library.

- NumPy
- Pandas
- Matplotlib
- SciKit-Learn
- [LightGBM Documentation](https://lightgbm.readthedocs.io/en/latest/Python-Intro.html) 

## Notebook

This report consist of three parts.

- Notebook1 : EDA
- Notebook2 : Preprocessing (feature engineering)
- Notebook3 : Modelling
