# Telangana-Kharif-Season-Rainfall-Classification
Predicting rainfall using Random Forest, Logistic Regression, Gaussian Naive Bayes, KNN, XGBoost, Support Vector Classifier.

<a rel="license" href="http://creativecommons.org/licenses/by/2.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/2.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/2.0/">Creative Commons Attribution 2.0 Generic License</a>.

# Motivation
Every year, the Kharif (Vaanakalam) season starts from June in Telangana State.

This kharif season starts with the onset of monsoon season from Mrigasira karti in Telangana State.

Mrigasira karti starts between the first/second week ie, 8th June normally in Telangana State. 

The main crops cultivated in kharif season are Paddy, all varieties of Millets, all varieties of  Pulses and Jowar which requires a moderate/normal rainfall for better yield.

The farmers of Telangana and Andhra States will be waiting with expectation of normal and moderate rainfall which will help them for sowing the seeds in Mrigasira karti with the onset of monsoon in June every year.

# Contents


*   Objective

*   Description of Dataset

*   Importing Libraries

*   Loading Data

*   Counting the number of null values

*   Imputing missing values using Multiple Imputation by Chained Equations(MICE)

*   Checking for Multicollinearity

*   Encoding 'Rain (mm)' to a categorical variable 

*   Checking for Outliers using Boxplot

*   Removing Outliers in Data using IQR

*   Declaring features and target variable

*   Scaling the data

*   Splitting the Data into train and test set

*   Balancing the Dataset using Synthetic Minority Oversampling Technique(SMOTE)

*   Fitting models using various ML algorithms(Random Forest, Logistic Regression, Gaussian Naive Bayes, K Nearest Neighbors, XGBoost, Support Vector Classifier), model evaluation and accuracy

*   Model Comparison using Accuracy

# Objective
The objective is to develop models that predict whether it will rain significantly or not based on meteorological measurements(Min Temp (°C),	Max Temp (°C),	Min Humidity (%),	Max Humidity (%),	Min Wind Speed (Kmph),	Max Wind Speed (Kmph)).

# Description of Dataset
This dataset is originally from the [Telangana's Open Data Platform](https://data.telangana.gov.in/) supported by the 'Open Data Policy' of the Government of Telangana.

This dataset provides information about the cumulative rainfall, minimum & maximum temperature, humidity & wind speed across all weather stations in the state of Telangana for the month of June in the year 2022.

The portal houses datasets form the various departments and organizations of the Government of Telangana.

The portal could be used by a variety of stakeholders and will enhance transparency in the working of the government apart from triggering innovative solutions to various problems.


*   'District': Name of the district,

*   'Mandal': Name of the Mandal,

*   'Date': Date in yyyy-mm-dd format,

*   'Rainfall (mm)': Cumulative Rainfall in mm,

*   'temp_min (⁰C)': Minimum Temperature in celcius,

*   'temp_max (⁰C)': Maximum Temperature in celcius,


*   'humidity_min (%)':Minimum Humidity %,


*   'humidity_max (%)': Maximum Humidity %,


*   'wind_speed_min (Kmph)': Minimum Wind Speed in kmph,


*   'wind_speed_max (Kmph)': Maximum Wind Speed in kmph.


In terms of rainfall, drizzle is typically defined as precipitation with an intensity of less than 1 mm per hour. In general, drizzle is considered to be a light and steady rainfall that doesn't produce much accumulation or cause significant impacts.

We encode values in feature "Rain (mm)" which are greater than 1 as '1' for rainfall and less than 1 as '0' for no rainfall and make a new categorical column 'rain_encoded' in dataframe


Finally, we observe that Random Forest and XGBoost performed better compared to other models. However, if speed is an important thing to consider, we can stick with Random Forest instead of XGBoost.
