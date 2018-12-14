# Investment Property Tool

## CS410 Project

Submitted By: Anish Abraham
Date        : December 14, 2018


## Project Overview:

There are several property websites where buyers can browse through properties listed for sale and get more details like viewing pictures and locations. However, property market is not very liquid and determining a fair price for a property is not very straightforward. 

An investor or even someone looking for a home and keen to personalize the home to their liking would prefer to purchase an undervalued home and spend money to personalize the property. It is always a challenge for the prospective buyer to determine whether the home which he is trying to buy is worth the money spent. 

This project tries to solve the problem by building a predictive model for finding the value with text retrieval and mining techniques. There are several websites which showcases the estimated price and the actual price of a property there by giving the customer a way to understand whether the amount they are spending is comparable to the estimated price of that property. Here we are trying to predict the value of the homes there by the customer will have a baseline for all the different homes irrespective of the location or the year in which it was built or the facilities available in that home. 

Zillow is one of the popular property listing websites in US. Using Zillow's GetUpdatedPropertyDetails API, we extracted the data. This data included details like full address, posting details, images, home facts such as bedrooms, bathrooms, year built, squarefoot, roof type, number of rooms, home description, neighborhood and school information.

### Problem Statement

Determining the value for money for a real estate property is not that easy. Different websites shows different estimated price for the same/ or similar property. This is primarily because of the way in which the features are being selected for obtaining the estimate. 

### Proposed Solution

The current property websites does not showcase the real value of a property which could be used to compare multiple properties. Hence we are trying to build a predictive model for finding the value by feature extraction involving textual data. The intended workflow for this project is mentioned below.

1. Extract the data from Zillow website using API GetUpdatedPropertyDetails.
    - Using the zillow ID , extract a range of data.
    - Store the deisred columns during the scraping process.
    - Validate the data before storing the field values.
    - Skip the values if the corresponding column is missing in the XML response.
    
2. Preprocess the data
    - Remove features which are not helpful for predicting the value.
    - Remove incomplete listings if the major feature values are missing.
    - Impute missing values: most frequent for text and median for others.
     
3. Feature Engineering
    - Topic modeling using LDA.
    - Convert corpus into Document Term Matrix
   
4. Build the model
    - Linear regression method is used to build the model.
    - Train the model
    
5. Test the model
    - Test the model built
    - Mean squared error is used for measuring model accuracy.

6. Explore other characterisitcs of the data
    - Bag of words representation
    - TF-IDF
    

Zillow_datafetch_API - This Jupyter notebook contains code to fetch real estate classified data from Zillow website using API. You need to use your own Zillow API key.
