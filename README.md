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
The project aimed at predicting the price of an Airbnb listing given a number of features. The project involved exploratory data analysis, data pre-processing, feature selection, Model Fitting, Model Comparison .

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

1. Check / prepare basic info of dataset

     drop not useful data

        a. drop all redundant/ duplicates data.
        b. drop all the column that contains same value , these data is not useful.
        c. drop columns that almost not containing any data.
        d. drop all the data the clearly will not help me during this jurney , like (Urls , reviewer  id , reviewer name ... ).

      Reduce the following wide catoigores

        a. Host Response Rate Grouped\
        b. Overall Rating
        c. Neighbourhood Grouped
        d. property_types
        e. Postal Code

      adding new data based on the existing data

        a. Calculate the distance of each listing from Berlin's center and join each listing to a group. Each group will contain listings that are within a specific distance from the center
        b. drop the following feature after using them to generate new one {'Host Since', 'neighbourhood', 'Latitude', 'Longitude', 'Property Type', 'Postal Code','Comments',Host Response Rate', 'Overall Rating','Instant Bookable', 'Is Superhost','Is Exact Location','Destance From Center Cleansed'}

