![image](https://user-images.githubusercontent.com/54724466/86974197-bb193500-c12a-11ea-8627-74118ff58984.png)

# **AIRBNB SAN FRANCISCO PRIVATE ROOMS** 


 Which neighborhoods in San Francisco offer tourists private rooms that fit their budget, are safe (crime-wise), close to Downtown and attractions?

 Let's find out what variables can help us discover which neighborhoods in San Francisco have the best (according to considerations above) private rooms to rent!

 This research aims to help tourists decide where their ideal locality will be  in “The Golden City”.
 
 
# **Phase 1 of analysis:**

The data was obtained from Kaggle, including 16 variables and 7833 observations. After data cleaning there are 7 variables and 2064 observations.

Variables considered were: Neighborhood, Price, reviews_per_month, reviews_total, availability_365, minimum_nights and calculated_host_listings_count.

Files first included:

**Listings.xlsx**- where all listings for Airbnbs in San Francisco are found. Including details like: number_id of listing, name, host_name, neighborhood, room_type, price, and many more interesting features.

**PrivateRooms.csv**- which includes all Airbnbs private rooms from listings. Including all details above.

**Reviews.csv**-includes listing_id and date of reviews.

Gathering necessary information from listings.xlsx...

Here is the Listings data frame: With 7833 observations of 16 variables
There are 2885 private rooms. Private rooms’ prices per night were decreased to $250.

