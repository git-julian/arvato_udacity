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
The main goal of this work is twofold.
First it aims to inevstigate the "unlabeld" datasets in order to find cirtain criteria that would differentiate a "typical" customer from the rest of the poulation. 
Secondly a supervised learning model should be trained in order to predict the likelihood of a customers response to it. 

In detail I investigated the following things in my work:

1. Understand and give an overview on the porvided datasets
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
* Udacity_MAILOUT_052018_TEST.csv - dataset to use the model on and participate on the Kaggle challenge

* DIAS Attributes - Values 2017.xlsx - information about columns
* DIAS Information Levels - Attributes 2017.xlsx - information about leves of the columns



## Results <a name="results"></a>

### 1. Understanding the data
The provided data is quite rich with 366 Features on the genereal population and customers set. 
There are however some challenges that needed to be taken care of. 
* The data has ambiguous missings. That could be solved by using the reference file to create consitant missing values.
* Besinde that the missings needed  to be handeld appropraite by dropping columns and rows of more than 90%.
* For the imputatiuon it was necessary to manually go through the dataset and check wich imputauon mehtod was bst for wich variable. 

### 2. Find Clsuters for customers and the gerneal population data

By using the elbow method it turen out that 13 clsuters would describe the data best.
Several clusters can be indetified in wich customer and the genereal data deviate. The highes deviation was found in the clusters 3, 4, 8, 9.

### 3. Wich features drive the difference

Looking deeper into clusters 8 and 9 it can be seen that customers are rather wealthy with a high intrest in financial topics and investment and living in cities. 
Conversly people in the gerneal poutation that are not likley to be customrs tend to have less money and more parsimonious.


### 4. Predict response for the e-mail campaign

For the classifcation task in a first approach RandomForrest, GradientBoostedTrees and XGBoost algorithem are testet without further optmization. 

*  RandomForrest perfromed worst with a AUC of 62% on the cross-validation score. It also overfitted the data the most. 
This however was a strong problem for all three alortihmes because of the highly inbalenced data. (Only 1.24% did Respond to the campaign.)

* The best perfomring model was XGBoost with an AUC of 93% on the training-set and 78% on the cross-validation set. 

Becaus of the inbalanced data the final training-set is rebalanced to a 33/66 proportin. This should avoid getting to much overfitting by the model wich can be seen in the learning-curves for the three models. 

### 5. Predicting test data and 

As a last stept the test data is scored with the trained model. 
Then a csv file conisting of the LNR-IDs and the predicted score is created.
After submitting the score to Kaggle a score of ca 0.69 is achieven. 



## Licensing, Authors, Acknowledgements <a name="licensing"></a>

The used data comes from Arvato BERTELSMANN provided by Udacity within their Nanodegree and can be only used in this context. All the licensing for the data and other information can be found on [Udacity](https://www.udacity.com/course/data-scientist-nanodegree--nd025).

[A blogpost to the work can be found here.](https://medium.com/@jbraun523_13616/know-your-customers-b9028c4edb8d)
