# TourismAnalysis
This project aims at analysing various tourism trends and answers to questions based on places  customers (with respect to adults/children) have most frequency of booking and travel, also the  most impactful channel for most number of bookings. The Expedia dataset, that we are using in this  project, contains their customer’s travel information like what they searched for, whether or not the  search result was a travel package, the check in and check out date. It aims at understanding user  and customer behavior with the data given in terms of tourism packages provided by Expedia.
# Motivation
Tourism has one of the major contribution for the GDP of a country. Tourism boards and companies 
in the tourism sector can benefit from big data in many ways. That includes offering packages 
tailored to visitors' likely interests, and deciding which countries to focus on winning customers in. 
These insights can be a great help in the decision-making process, and improve how the tourism 
industry operates. Players in the tourism industry can now make informed decisions on the basis of 
analytics and number-driven data. They can identify targeted groups of potential customers at every 
stage in the trip planning process. They can also increase efficiency and the quality of services. Big 
data can even be used to predict which new products might work well in their market.
# Objectives
1. Analysis on various tourism trends and answers to questions based on places customers 
(with respect to adults/children) have most frequency of booking and travel, also the most 
impactful channel for most number of bookings
2. Feature engineering to shape raw data to useful data such as: duration of stay in hotels, 
number of days between booking and staying in hotel and check-in time stamp
3. Finding most popular hotel clusters for each destination 
# Data Pre-processing
The first step is to clean and pre-process the data and perform exploratory analysis to get some 
interesting insights into the process of choosing a hotel.
 The users who did not booked the hotel are removed
 The searches by each user belonging to a specific type of destination are identified
 The check-in and check-out dates are found to find the duration of the stay for each of 
the entries in the training set.
# Feature Engineering
Feature engineering is the process of using domain knowledge to extract features from raw 
data. A feature is a property shared by independent units on which analysis or prediction is to be 
done. Features are used by predictive models and influence results. This is performed to extract 
useful data from the raw data. We are trying to find
 duration of stay in hotels
 number of days between booking and staying in hotel
 check-in and check-out time stamp
Plots for books as per day, month and year are performed.
# Analyse
We have implemented a solution with pandas to find the "most popular local hotel" using the 
datasets available and provide recommendation results.
Step 1
Read in the train data using only the necessary columns. Specifying datatypes helps reduce 
memory requirements. The file is read in chunks of 1 million rows each. In each chunk we count 
the number of rows and number of bookings for every destination-hotel cluster combination.
Step 2
Next we aggregate again to compute the total number of bookings over all chunks. Compute the 
number of clicks by subtracting the number of bookings from total row counts. Compute the 
'relevance' of a hotel cluster with a weighted sum of bookings and clicks.
Step 3
Read in the test data and merge most popular hotel clusters
