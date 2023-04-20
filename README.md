
##Discogs Price Prediction Model

This repository contains code for a machine learning model that predicts the prices of vinyl records on Discogs based on generes and various attributes of the record such as the artist, release year, genre, condition, and more.

##Requirements:

Python 3
pandas
scikit-learn
numpy
Data

The data used for training and testing the model was obtained from the Discogs Marketplace scraper (https://github.com/grigorjevas/Discogs-marketplace-scraper)which can give you a dataframe of 10,000 records maximum by generes.

The data that was collected includes information on over  vinyl 8000 records from various genres and artists.

##Usage-

To train the model, run the script. This script will preprocess the data, split it into training and testing sets, and train the model using a LinearRegression, random forest algorithm and trying to make a better result with Hyperparameters and cross validation.

To make predictions using the trained model, run the models script and provide it with the necessary inputs such as the artist, release year, genre, and condition of the record. The script will then output a predicted price for the record based on the model.

##Evaluation-

The accuracy of the model was evaluated using mean absolute error (MAE) and mean squared error (MSE) metrics on a held-out test set. The resulting MAE was X and the resulting MSE was Y.

##Model-
The model was trained using Jupiter/Python notebook in this repository. Model accuracy results are provided below..

with Hyperparameters- 

Mean Squared Error: 485.17
R2 Score: 0.48

RandomForestRegressor- 

ValType	R2-Score	MSE	RMSE
0	Train	0.914136	122.972904	11.089315
1	Test	0.455929	510.968876	22.604621

##Conclusion-
This model can be used by vinyl record collectors and sellers to get an estimate of the value of a particular record before buying or selling it on Discogs.

The results are not great but as they will probably will not work as good with new data but it opened alot of other questions or ideas for the future, such as estimating your collection worth and I will continue with this project as it shows potential for record shops as it will ease the online pricing process. 
