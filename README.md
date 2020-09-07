# ### Table of Contents

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
The main goal of this work is twofold.
First it aims to inevstigate the "unlabeld" datasets in order to find cirtain criteria that would differentiate a "typical" customer from the rest of the poulation. 
Secondly a supervised learning model should be trained in order to predict the likelihood of a customers response to it. 

In detail i investigated the following things in my work:

1. Dnderstand and give an overview on the porvided datasets
2. Find clsuters in wich customers and the general popualtion deviate the most. 
3. Give an indication based on the underlying features what factors may differentiatie customers from non-cunstomers. 
4. Prdeict the response of the mail campaign 
5. Get a decent score on the accompanied kaggle challenge. 

## File Descriptions <a name="files"></a>

All of the above described points are implemente in one jupyther notebook. "Arvato_Project_Workbook.ipynb"
Besinde that for read only there is also an HTML version of this notebook provided. 

Because of the terms and conditions of this project the data ist not provide in this git repo. 

The fils to run this notebook are the follwoing:

* Udacity_AZDIAS_052018.csv - unlabeld dataset of the general popualtion
* Udacity_CUSTOMERS_052018.csv - unlabeld dataset of the arvato customers
* Udacity_MAILOUT_052018_TRAIN.csv - labeled data set for supervised model training

* DIAS Attributes - Values 2017.xlsx - information about columns
* DIAS Information Levels - Attributes 2017.xlsx - information about leves of the columns
