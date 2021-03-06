# Arvato Capstone Project - Customer Segmentation and Prediction

### Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Project organization](#organization)
4. [Installation](#installation)
5. [Results](#results)
6. [Acknowledgements](#acknowledgements)
7. [References](#references)

## Introduction<a name="introduction"></a>
In this project, we work with Arvato's datasets[1] to provide a solution to the customer segmentation/prediction problem of a mail-order sales company. Various machine learning techniques are applied to identify the customers for a marketing campaign of the company. 

The project contains three main steps:

0. **Data exploration analysis:** Use techniques to explore and clean the demographics data for the general population of Germany (referred to as the Azdias dataset) and the demographics for customers (referred to as the Customer dataset). 
1. **Customer segmentation task:** Apply data scaling, PDA and K-Means clustering on the Azdias/Customer datasets to describe the core customer base of the company and to identify the common characteristics of customers.
2. **Customer prediction task:** Leverage insights observed in the previous parts to develop a supervised learning model that could predict whether an individual would respond to a mail campaign.

As the last step of the project, the prediction result from Part 2 is submitted to Kaggle[2] and compared against other submissions.

## Dataset<a name="data"></a>
In this project, Arvato provides us four demographic files. Each file contains one dataset and in CSV (Comma-separated values) format, in which each row represents demographics of an individual and each column represents an attribute.
*	Udacity_AZDIAS_052018.csv: Demographics data for the general population of Germany; 891,211 persons (rows) x 366 features (columns),
*	Udacity_CUSTOMERS_052018.csv: Demographics data for customers of the mail-order company; 191,652 persons (rows) x 369 features (columns),
*	Udacity_MAILOUT_052018_TRAIN.csv: Demographics data for individuals who were targets of a marketing campaign; 42,982 persons (rows) x 367 (columns),
*	Udacity_MAILOUT_052018_TEST.csv: Demographics data for individuals who were targets of a marketing campaign; 42,833 persons (rows) x 366 (columns). 

## Project organization<a name="organization"></a>
1. `data/:` folder that contains the datasets (4 files) with their metadata files (2 files). This folder also includes (i) PKL files of proceed datasets for fast loading data and (ii) _features-final.csv_ created after finishing data exploration. As part of the terms and conditions of using datasets, I am not allowed to include them in this repository.
2. `model/:` folder that contains all developed models.
3. `cache/:` folder that contains parameters during model development.
4. `Arvato_project_workbook.ipynb:` the main notebook that presents all steps of the project.
5. `report.pdf:` the final report submitted to Arvato. Note that the report is associated with the first run of the notebook, so some of results may be slightly different.

## Installation<a name="installation"></a>
The project is conducted using Amazon SageMaker and then tested in my local machine. 
Besides the libraries included in the Anaconda distribution for Python 3.6 the following libraries have been included in this project:
* `progressbar` - library to display progressbar
* `lightgbm` - gradient boosting framework that uses tree based learning algorithms.
* `py-xgboost` - optimized distributed gradient boosting library designed to be highly efficient, flexible and portable.

To install the above libraries from Jupyter Notebook:
```
%conda install -c conda-forge lightgbm progressbar py-xgboost -y
```

As stated above the data for this project is not public, the notebook and models provided by this repository cannot be used but they serve as a snapshot of the capstone project.

## Results<a name="results"></a>
The model has a score of 0.792 that is only 0.018 smaller than the best score recorded on Kaggle competition.

## Acknowledgements<a name="acknowledgements"></a>
My sincere gratitude to Arvato Financial Solutions for the datasets/files and to Udacity for making this project possible.

## References<a name="references"></a>
[1] [Arvato Financial](https://finance.arvato.com)

[2] [Kaggle Prediction Competition](https://www.kaggle.com/c/udacity-arvato-identify-customers)
