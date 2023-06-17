# Enhancing-Supply-Demand-Forecasting-for-Optimal-Ride-Booking-Services
Problem Understanding and Problem Formulation:
The above scenario describes a problem faced by the ride-hailing company, which needs to predict the
demand-supply gap in different regions of a city at different time slots. This prediction is crucial for
ensuring that there are enough drivers available to meet the demand of passengers and to prevent surge
pricing. The problem is complex and requires processing large amounts of data, including information
about the number of ride requests and driver acceptances in each region and time slot. The problem can
be formulated as a regression task, where the goal is to predict the gap between ride requests and driver
acceptances. The evaluation metric used for this problem is mean absolute error, which measures the
average difference between the predicted and actual gap values. Solving this problem requiresthe use of
machine learning algorithms and data analysis techniques.
Data Understanding and Preparation:
The Data in the test folder was extracted and read into the file. There were 21 files for order and
weather data. The order data were extracted to 8.5 million rows. The weather data was extracted to
about 5000 rows. First I merged these tables as per the nearest time slot of the order data table as
corresponding to the weather table. Then I read the cluster map and replaced the hash values with their
ids. Finally having the data frame including weather, order and the respective hash values I de structured
the date time object into its respective components and appended to the data frame. Furthermore I
calculated the time slots by multiplying the hours with 6 adding them to the result of dividing the
minutes by 10. This gave the specific time slots. After that I used group by and prepared the data for the
model to be trained on.
Feature Engineering:
In feature engineering I have used the columns from the respective weather table including
Temperature, PM2.5. Also we used the startRegionHash, date and timeslot to calculate the demand and
supply columns which in return create the gap column.
