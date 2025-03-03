# Price Prediction of Berlin Airbnb accommodation

Project created at March 2025.

The datasets contain detailed listings data of current Airbnb listings in Berlin. <br>
The goal is to predict the Price of accomodation by Summary information. (Regression problem)<br>
 <br>
The dataset has 66833 rows and 48 columns, this is only 2019 data, reduced the data due to its size
 <br>

The columns before doing any preperation / EDA 



RangeIndex: 66833 entries, 0 to 66832   
Data columns (total 48 columns):   
 #   Column                 Non-Null Count  Dtype       
---  ------     §            --------------  -----    
 0   Review ID              66833 non-null  float64  
 1   Reviewer ID            66833 non-null  float64  
 2   Reviewer Name          66833 non-null  object   
 3   Comments               66782 non-null  object   
 4   Listing ID             66833 non-null  int64    
 5   Listing URL            66833 non-null  object   
 6   Listing Name           66817 non-null  object   
 7   Host ID                66833 non-null  int64    
 8   Host URL               66833 non-null  object  
 9   Host Name              66833 non-null  object   
 10  Host Since             66833 non-null  object   
 11  Host Response Time     65868 non-null  object   
 12  Host Response Rate     65868 non-null  object   
 13  Is Superhost           66833 non-null  object   
 14  neighbourhood          66833 non-null  object   
 15  Neighborhood Group     66833 non-null  object   
 16  City                   66824 non-null  object   
 17  Postal Code            65737 non-null  object   
 18  Country Code           66833 non-null  object   
 19  Country                66833 non-null  object   
 20  Latitude               66833 non-null  float64  
 21  Longitude              66833 non-null  float64  
 22  Is Exact Location      66833 non-null  object   
 23  Property Type          66833 non-null  object   
 24  Room Type              66833 non-null  object   
 25  Accomodates            66833 non-null  int64    
 26  Bathrooms              66791 non-null  float64  
 27  Bedrooms               66763 non-null  float64  
 28  Beds                   66829 non-null  float64  
 29  Square Feet            2071 non-null   float64  
 30  Price                  66833 non-null  object   
 31  Guests Included        66833 non-null  int64    
 32  Min Nights             66833 non-null  int64   
 33  Reviews                66833 non-null  int64   
 34  First Review           66833 non-null  object  
 35  Last Review            66833 non-null  object  
 36  Overall Rating         66719 non-null  float64  
 37  Accuracy Rating        66719 non-null  float64  
 38  Cleanliness Rating     66719 non-null  float64  
 39  Checkin Rating         66719 non-null  float64  
 40  Communication Rating   66719 non-null  float64  
 41  Location Rating        66719 non-null  float64   
 42  Value Rating           66719 non-null  float64  
 43  Instant Bookable       66833 non-null  object   
 44  Business Travel Ready  66833 non-null  object   
 45  year                   66833 non-null  int64    
 46  month                  66833 non-null  int64    
 47  day                    66833 non-null  int64    

References: <br>
[Kaggle Berlin Airbnb Data Sources](https://www.kaggle.com/datasets/thedevastator/berlin-airbnb-ratings-how-hosts-measure-up) <br>

#### Task: 

1. Check basic info of dataset
<br><br>
2. Deal with Outlinear and Missing Value

        a. Exclude outliner from price data
        b. deal with missing values of features
<br>
3. perform Exploratory Data Analysis (EDA)

        a. Location vs Price
        b. room and property type vs Price
        c. Price Differences on a minimum_nights, number_of_reviews, reviews_per_month, and availability_365
        d. Correlations between reviews

<br>
4. Data Preprocessing on features

        a. Transfer 'latitude' and 'longitude' to the 'distance' from center
        b. Transfer data "amenities"
        c. Transfer 'interaction', and 'instant_bookable' data into bool
        d. drop the columns that is not helpful for prediction
        e. convert all string columns into categorical or numerical data 
        f. One-hot encoding on categorical features

<br>
5. Build ML Models 

        a. Linear Regression
        b. Random Forest
        c. XGBoost Regressor
        
#### Prediction result on Testing Set

1. linear regressor: R^2 = 0.4191
2. Random Forest Regressor: R^2 =  0.5170
3. XGBoost Regressor: R^2 = 0.5622

![subsmission result](https://github.com/vivianchang2019/Berlin_Airbnb_Price_Prediction/blob/master/result/Airbnb_feature_importance.JPG?raw=true)