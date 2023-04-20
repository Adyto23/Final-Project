
**Discogs Price Prediction Model**

**Ady Toledano**  
**IronHack, Remote Course, Berlin 24 Mar 2023**

**Overview**

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

**Usage**

To train the model, run the script. This script will preprocess the data, split it into training and testing sets, and train the model using a LinearRegression, random forest algorithm and trying to make a better result with Hyperparameters and cross validation.

To make predictions using the trained model, run the models script and provide it with the necessary inputs such as the artist, release year, genre, and condition of the record. The script will then output a predicted price for the record based on the model.

## Data information**

* 13 columns 
* 7698 rows 
* columns:

| Initial Column | Comments 

* 'artist' - Both artist and title are dropped as they are quite unique 
* 'title' - Both artist and title are dropped as they are quite unique 
* 'release_format' - what format is the release at: 12", 7", LP , Compilation , CD , Digital
* 'number_of_tracks' 
* 'price'- price in dollars was edited to float
* 'rating' - a grade to the release by number
* 'votes' - probably should be dropped 
* 'have'- How many people have this record 
* 'want'- how many people added to their Want List 
* 'limited_edition' - 0 - not limited , 1 - limited edition release 
* 'media_condition'- shows information about the Media condition please see new columns for the rate mapper 
* 'sleeve_condition' - shows information about the Sleeve condition please see new columns for the rate mapper 
* 'release_page' - URL of the release , was dropped in the process
* 'release_date' - shows Day , Month and  Year and got dropped as we used only year
* 'label'	- this column is showing the label name and code , was split to two columns

| New Column |
* 'genre'- was added in the scrating process 
* 'label_name'- label name was kept was it might be similar to some releases 
* 'label_code'- though this was created , we choose to remove it from the dataframe 
* 'year'- as the day and month in release_date are not filled we selected only the year which will give a bit more correlations 
* 'sleeve_condition_scale' - scale_mapper_sleeve = {"M":1, "NM ":2, "VG+":3, "VG":4 , "G+": 5, "G":6 , "F": 7,"P": 8, "no cover": 9}
* 'media_condition_scale' - scale_mapper_record = {"M":1, "NM ":2, "VG+":3, "VG":4 , "G+": 5, "G":6 , "F": 7,"P": "8"}


**Evaluation**

The accuracy of the model was evaluated using mean absolute error (MAE) and mean squared error (MSE) metrics on a held-out test set. The resulting MAE was X and the resulting MSE was Y.

## Model-
The model was trained using Jupiter/Python notebook in this repository. Model accuracy results are provided below..

## with Hyperparameters- 

* Mean Squared Error: 485.17
* R2 Score: 0.48

## RandomForestRegressor- 

ValType	R2-Score	  MSE	        RMSE
***************************************
0	Train	0.914136	122.972904	11.089315
***************************************
1	Test	0.455929	510.968876	22.604621


**Conclusion**

This model can be used by vinyl record collectors and sellers to get an estimate of the value of a particular record before buying or selling it on Discogs.

The results are not great but as they will probably will not work as good with new data but it opened alot of other questions or ideas for the future, such as estimating your collection worth and I will continue with this project as it shows potential for record shops as it will ease the online pricing process. 
