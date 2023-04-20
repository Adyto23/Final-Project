
**Discogs Price Prediction Model**
**Ady Toledano**  
**IronHack, Remote Course, Berlin 24 Mar 2023**

## Overview

This repository contains code for a machine learning model that predicts the prices of vinyl records on Discogs based on generes and various attributes of the record such as the artist, release year, genre, condition, and more.

## Used:

* Jupyter Notebook
  Python 
  pandas
  scikit-learn
  numpy
  Data
* Hypothesis Testing 
* Data visualization
* Tableau


The data used for training and testing the model was obtained from the Discogs Marketplace scraper (https://github.com/grigorjevas/Discogs-marketplace-scraper)which can give you a dataframe of 10,000 records maximum by generes.

The data that was collected includes information on over  vinyl 8000 records from various genres and artists.

**Usage-

To train the model, run the script. This script will preprocess the data, split it into training and testing sets, and train the model using a LinearRegression, random forest algorithm and trying to make a better result with Hyperparameters and cross validation.

To make predictions using the trained model, run the models script and provide it with the necessary inputs such as the artist, release year, genre, and condition of the record. The script will then output a predicted price for the record based on the model.

## Data information-

* 10 columns 
* 1222997 rows 
* columns:
* 
| Initial Column | Comments | New Column |
Id - Wikidata Id
Name - Full Name
Short description - Will detail the Profession of the person and should they have more than one it will be listed in this column, in this column I have tried to sum it to one Profession in order to get a more clear view
Gender - Gender / Sex
Country - Country / historical region, deleted in this column countries after the charecter ";" in order to get a better overview in the data
Occupation - Occupation title
Birth year - Birth year
Death year - Death year, limiting this column to years above 1930
Manner of death - Such as suicide, natural causes or capital punishment
Age of death - Age of death , changing the range to between 18-100
AgeRange - New column created for ranges: 18-29, 30-39, 40-49, 50-59, 70+

**Evaluation-

The accuracy of the model was evaluated using mean absolute error (MAE) and mean squared error (MSE) metrics on a held-out test set. The resulting MAE was X and the resulting MSE was Y.

## Model-
The model was trained using Jupiter/Python notebook in this repository. Model accuracy results are provided below..

## with Hyperparameters- 

Mean Squared Error: 485.17
****************************
R2 Score: 0.48

## RandomForestRegressor- 

ValType	R2-Score	  MSE	        RMSE
***************************************
0	Train	0.914136	122.972904	11.089315
***************************************
1	Test	0.455929	510.968876	22.604621


**Conclusion-

This model can be used by vinyl record collectors and sellers to get an estimate of the value of a particular record before buying or selling it on Discogs.

The results are not great but as they will probably will not work as good with new data but it opened alot of other questions or ideas for the future, such as estimating your collection worth and I will continue with this project as it shows potential for record shops as it will ease the online pricing process. 
