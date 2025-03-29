# Price Prediction of Berlin Airbnb accommodation

Project created at March 2025.

## Project Overview: Predicting Airbnb Listing Price Using Machine Learning


## Research Question:
In a given set of features of an apartment located in Berlin, such as neighborhood, number of beds, bathrooms, accommodates, minimum nights, and more, we can predict the Airbnb price.

The goal of this project is to provide price predictions for Airbnb listings based on various attributes and features, including the number of beds, neighborhood, accommodates, and more. This analysis is based on a dataset of over 23,000 apartments with more than 450,000 reviews.

The project will explore the relationship between these features by exploratory data analysis, data pre-processing, feature selection, Model Fitting, Model Comparison and use them to predict the price.

Finally, we will develop an interactive system that accepts different listing features and provides an estimated Airbnb price

References: 
[Kaggle Berlin Airbnb Data Sources](https://www.kaggle.com/datasets/thedevastator/berlin-airbnb-ratings-how-hosts-measure-up) 

## Dataset Overview:
The Berlin Airbnb dataset contains over 450,000 apartment reviews for 23,000 different listings from the years 2009 to 2018.
The dataset includes features that describe each listing, such as location, neighborhood, number of beds, and more. We can observe that each apartment has tens or even hundreds of reviews. Therefore, it is necessary to clean, fix, and aggregate these reviews into a single entry per apartment

## Project Goals:

The goal is to predict the price of an Airbnb listing in Berlin based on various features such as location, number of beds, bathrooms, and other characteristics. The project will explore the relationship between these features through exploratory data analysis, data preprocessing, feature selection, model fitting, and model comparison, ultimately using them to predict the price.

Success is defined as the ability to predict the listing price in Berlin Airbnb as accurately as possible based on different features.


# Data Preparation:

1.    **Data Aggregation**:  Aggregate the data make it contain only one row per listing. The current data includes multiple reviews for each listing, so aggregation was performed. For each column, we determined whether to take the mean, last values, or concatenate strings. This action reduced the dataset from 450,000 rows to 23,000 rows.
    
2.  **Removing Redundant Data**: dropping redundant and duplicated data. Certain features can be clearly identified as duplicates or redundant and have very high cardinality, such as 'Review ID', 'Reviewer ID', 'Reviewer Name', 'Listing URL', 'Listing Name', 'Host ID', 'Host URL', 'Host Name', 'City', 'Country Code', 'Country', 'First Review', and 'Last Review'. Additionally, features that contain a single value throughout the dataset, like "Business Travel Ready," which only has the value "f," were also removed.
    
3.  **Data Cleaning**:  Cleaning and fixing erroneous values by deleting punctuation marks, such as removing "$" and "%" from prices, and correcting typos in the textual data.
    
4.  **Standardizing Boolean Values**: We transformed non-standard boolean representations into standard booleans, changing "t" to "true," for example.
    
5.  **Running AutoVIS**: Ran AutoVIS on the dataset, which generated a detailed report that includes a wide range of graphical diagrams. The report provided information for each column, detailing missing values, cardinality, data types, scatter plots for each feature against the target feature "price," and the distribution for each feature relative to the target value of price.


# Exploratory Data Analysis (EDA):


During the EDA phase, we performed a visual exploration of relationships between continuous features and categorical variables in relation to the target variable, popularity. Various visualizations were used to identify trends and patterns in the features.

In this stage, we accomplished the following:

-   By calculating skewness, we analyzed the data distribution and identified where outliers reside.
    
-   This stage helped uncover potential relationships between features that could influence the target variable (price), such as insights from the Spearman heatmap.
    
-   Identified outlier boundaries and marked all outliers for deletion in the subsequent steps. Additionally, we examined how the data distribution changed before and after outlier removal.
    
-   Identified missing values and removed empty features or features with more than 60% missing values.
    
-   Performing data imputation using KNN.

# Feature Engineering:
After cleaning and filling the missing data , in this stage we will enrich the data with relevant information that will affect the prediction model.

- draw the Berlin listing map  , 
![Berlin Listings Map](https://github.com/rafatb/Berlin_Airbnb_Price_Prediction/blob/main/files/berlin-maps.png)

- expose the most used words from the comment feature 
![Berlin words](https://github.com/rafatb/Berlin_Airbnb_Price_Prediction/blob/main/files/berlin-words.png)

- calculate List distance from Berlin center and divide Berlin to circles each circle have specific distance from the center like (2km , 4km , 6km .....) , this new feature maybe will have an impact on the target Price.
- get Listing years old - how much this Listing is in the Airbnb.
- reduce categories , in this case we dropped Neighborhood because it have too much categories and keep the  Neighborhood Group because its with few categories.   
-  
