# Airbnb-San-Francisco-Private-Rooms

Which neighborhood in San Francisco offers tourists private rooms that fit their budge, is safe, is close to Downtown and attractions? 

Let's find out what varibles can help us discover which neighborhood in San Francisco has the best(according to considerations above) private rooms to rent!

This research aims to help tourists decide which neighborhood in San Francisco has the best private rooms to rent.yn The
data was obtained from Kaggle, including 16 variables and 7834 observations. After data cleaning there are 7 variables and 2064 abservations.
Variables considerated were: Neighborhood, Price, reviews_per_month, reviews_total, availability_365,  minimum_nights and calculated_host_listings_count.

Files included were: listings.xlsx, PrivateRooms.csv, PrivateRooms.xlsx, reviews.csv.

Gathering necessary information from listings.xlsx...

There were initially 2885 private rooms. Neighborhoods that were excluded which had fewer private rooms to rent: Neighborhoods with <20 private rooms:
## Presidio, Golden Gate Park, Diamond Heights, Presidio Heights, Seacliff, Glen park

Private rooms' prices per night was decreased to $250 and now boxplot(privaterooms$price) has fewer outliers.
Boxplots were also created for minimum_nights, reviews_per_month, reviews_total, calculated_host_listings_count and availability_365.
After closely observing those boxplots, outliers were removed together as well as NA values.
Those boxplots now present a cleaner organization of the PrivateRooms.csv data.


##MAKE NUMERICAL NEIBORHOODS, CATEGORICAL, 1-10, PUTTING THE SIMILARS TOGETHER. rUN A LINEAR REGRESSION MODEL ON IT.





