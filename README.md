### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Methodology](#methodology)
5. [Results](#results)
6. [Discussion](#discussion)
7. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

To run just an anaconda verison is needed. It holds most of the packages used by default.
Beside that you will need to make sure that xgboosting is installed on your mashine. 
## Project Motivation <a name="motivation"></a>

This project was created as a final capstone proejct of a Data Science course offerd by Udacity. The used dataset is provided by arvato a german service company. The data consits of three major pars.
First an dataset on german population, having different variabes that describe socio-economical attributes of the overall german population. Secondly there exists a second datast with almost the same featurs but this time specificly for customers of arvato.
The third dataset is alos has the same features as described above but alos holds a variable if a customer responded to a mailing campaign in the past.
These datasets preprocessed in order to work on the two major goals of this work. 
The main goals are the following:
First it aims to inevstigate the "unlabeld" datasets in order to find cirtain criteria that would differentiate a "typical" customer from the rest of the poulation. 
Secondly a supervised learning model should be trained in order to predict the likelihood of a customers response to it. 

I structured this notebook in the follwoing way: 
A. Import needed packages

B. Define custom functions that are used in the Notebook 

   0.Inspect the dataset
*   0.1 Load the data
*   0.2 Inspect the datasets
*   0.3 Develop Feature Engineering
*   0.4 Feature Eng. Pipeline

1. Customer Segmentation Report 
* 1.1  PCA as Preperation
* 1.2  Perfrom Clustering
* 1.3  Result interpretation

2. Supervised learning Model
* 2.1 Load and investigate data
* 2.2 Build ML-Pipeline to thest diffrent algorithms
* 2.3 Optimize selected model

3. Kaggle Competition
* 3.1 Score data
* 3.2 Create export for Kaggle 


## File Descriptions <a name="files"></a>

All of the above described points are implemente in one jupyther notebook. "Arvato_Project_Workbook.ipynb"
Besinde that for read only there is also an HTML version of this notebook provided. 

Because of the terms and conditions of this project the data ist not provide in this git repo. 

The fils to run this notebook are the follwoing:

* Udacity_AZDIAS_052018.csv - unlabeld dataset of the general popualtion
* Udacity_CUSTOMERS_052018.csv - unlabeld dataset of the arvato customers
* Udacity_MAILOUT_052018_TRAIN.csv - labeled data set for supervised model training
* Udacity_MAILOUT_052018_TEST.csv - dataset to use the model on and participate on the Kaggle challenge

To load in the data smoothy abve datasets with the code at habd one must place the above files in a folder named "data" that is located in the same directory as the jupyter notebook.

* DIAS Attributes - Values 2017.xlsx - information about columns
* DIAS Information Levels - Attributes 2017.xlsx - information about leves of the columns

To load the Excel files with the given code they must be placed in the same direcory as the notebook. 

## Results <a name="results"></a>

[A detailed description of the results can be find in my blogpost.](https://medium.com/@jbraun523_13616/know-your-customers-b9028c4edb8d)


## Licensing, Authors, Acknowledgements <a name="licensing"></a>

The used data comes from Arvato BERTELSMANN provided by Udacity within their Nanodegree and can be only used in this context. All the licensing for the data and other information can be found on [Udacity](https://www.udacity.com/course/data-scientist-nanodegree--nd025).

