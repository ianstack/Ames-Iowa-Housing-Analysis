# <span style="font-variant:small-caps;">Project 2 - Ames Housing Data and Kaggle Challenge:</span>
#### <span style="font-variant:small-caps;">Ian Stack</span>

---

## Executive Summary

### Contents:
-[Problem Statement](#Problem-Statement)

-[Description of Data](#Description-of-Data)

-[Conclusion and Recommendations](#Conclusion-and-Recomendations)

---
### <span style="font-variant:small-caps;">Problem Statement</span> 
*I was hired by the Iowa Housing company to asses the Ames Iowa housing dataset in order to find out which attributes of a home are most important when buying and selling a home to make profit. This process, commonly known as flipping houses, can be a lucrative investment strategy but it also carries a certain level of risk. In order to successfully flip houses, I will analyze the Ames Iowa housing dataset and determine which qualities of the homes attribute to a higher sale price.*

I will use linear, ridge, and LASSO regression models to predict the sale price for properties in Ames Iowa housing dataset. The measurement I will use to predict the sale prices will be the root mean squared error (RMSE) from the regression problems.

### Goal

With the provided datasets, predict the sale price for each home in the Ames Iowa Housing dataset based of their 'Id.'

### Description of Data

#### Datasets
I was orginally given two datasets: ['train.csv'](./datasets/train.csv) and ['test.csv'](./datasets/test.csv).  During my analysis I split up the ['train.csv'](./datasets/train.csv) into 3 other datasets.  Furthermore, I created the ['Saleprice.csv'](./datasets/SalePrice.csv) which has the "Id" and "SalePrice."  Lastly, I created submission files that I used to submit on the Kaggle website.  All of datasets are located in the dataset folder.
 

#### Source
Provided from the project-02-main Datasets:
- [`train.csv`](./datasets/train.csv): Ames Housing Training Dataset
- [`test.csv`](./datasets/test.csv): Ames Housing Testing Dataset


### <span style="font-variant:small-caps;">Data Dictionary</span>
The full data ditionary can be found at ([Kaggle](https://www.kaggle.com/c/dsirfx817/data)).
One-hot encoding was used on object type features, creating numerous new columns however not all were included in modeling process.  However, all of the new columsn were derived from the ones located on the link provided above. 

### <span style="font-variant:small-caps;">Brief Analysis</span>
I started my analysis by looking over the given datasets and data dictionary to see all the different features and values.  Looking at the Ames Iowa housing dataset presented from Kaggle, I will look for trends between features and sale price.


### <span style="font-variant:small-caps;">Model Performance on Training/Test Data</span>
In total I fitted 7 different models using 3 unique sets of features.  In the table below you can see which regression technique I used, the RMSE score for the training and test set. 

|Model|Regression Type|RMSE Train Score|RMSE Test Score|
|---|---|---|---|
|Model 1|Linear Regression|28527.83|31253.94|
|Model 1|Lasso Regression|28267.13|26828.42|
|Model 1|Ridge Regression|28220.04|26946.72|
|Model 2|Linear Regression|26859.52|27442.81|
|Model 2|Lasso Regression|27675.73|26172.22|
|Model 3|Linear Regression|23515.38|24741.02|
|Model 3|Lasso Regression|24825.39|23366.27|


### <span style="font-variant:small-caps;">Conclusions and Recommendations</span>

Upon performing this analysis, we are able to come to certain conclusions:
1. This statiscal analysis of the Ames Iowa Housing dataset showed lower RMSE scores when utilizing Linear and Lasso regression.
2. The Lasso function imposed a constraint on the model parameters, eliminating features with a low or 0 coefficients.
3. The Root Mean Square Error(RMSE) was typically lower when comparing the LASSO regression model to the Linear regression model.  
4. The results showed that the LASSO regression outperformed the Ridge and Linear Regression functions.  This is due to the fact in the LASSO  regression it shirnks values realtively low or close to 0 coefficients.
5. Starting from baseline, the RMSE decreased from model 1, 2, and 3 respectively.
6. Adding different features, a combination of numerical and categorical decreased the RMSE


And from these conclusions, we can make recommendations:

My recommendations based off my anaylsis of the Iowa Housing dataset for the Iowa Housing Company include:

Based on the run models there are 5 features that will be the most impactful towards sale price:

    - Overall material and quality of property
    - Ground Living Area
    - Total Basement Square Footage
    - Neighborhoods:StoneBr, NridgHt, NoRidge

When remodeling a home it is important that the overall material and quaility of the property is very good or excellent.
Furhermore, one should pay attention to specific neighborhoods specifically: Stone Brook, Northridge Heights, and 
Northrdige.  It is also important to make inspect the overall size of the living room and basement.

Lastly, two features produced negative coefficients which tells us that the worsening of these features, lowers
the sale price.  They are kitchen quality and exterior quality.  It is important the quality and condition of the 
kitchen and exterior quality is average or good.  

Overall for someone who is buying and selling a home, inspecting the listed features above will help ensure the
best saleprice. 