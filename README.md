# Price Prediction of Berlin Airbnb accommodation

Project created at March 2025.

The datasets contain detailed listings data of current Airbnb listings in Berlin for years 2019. <br>
The goal is to predict the Price of accomodation by Summary information. (Regression problem)<br>
 <br>
The dataset has 66833 rows and 48 columns, this is only 2019 data, reduced the data due to its size
 <br>


## Project Resources
<div class="row">
	  <ul>
	    <li><a href="https://www.kaggle.com/datasets/thedevastator/berlin-airbnb-ratings-how-hosts-measure-up">Airbnb Dataset</a> used in the project</li>
	    <li>View Source on <a href="https://github.com/rafatb/Berlin_Airbnb_Price_Prediction.git">Github</a></li>
	  </ul>
</div>


# Project Report: Predictive Price Modeling for Airbnb listings
The project aimed at predicting the price of an Airbnb listing given a number of features. The project involved exploratory data analysis, data pre-processing, feature selection, Model Fitting, Model Comparison and deploying the containerised Webapp on AWS using CI/CD Pipeline.

## Project Goals and Objectives
<div class="row">
      <p style="margin-top:0px;">The Short Answer: Assisting Airbnb hosts to set appropriate price for their listings</p>
      <p class="p_no_top_gap">
        <b>The Problem</b>: Currently there is no convenient way for a new Airbnb host to decide the price of his or her listing. New hosts must often rely on the price of neighbouring listings when deciding on the price of their own listing.
      </p>
      <p class="p_no_top_gap">
        <b>The Solution</b>: A Predictive Price Modelling tool whereby a new host can enter all the relevant details such as location of the listing, listing properties.. etc and the Machine Learning Model will suggest the Price for the listing. The Model would have previously been trained on similar data from already existing Airbnb listings.
      </p>
 </div>


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
        b. Transfer 'interaction', and 'instant_bookable' data into bool
        c. drop the columns that is not helpful for prediction
        d. convert all string columns into categorical or numerical data 
        e. One-hot encoding on categorical features

<br>
