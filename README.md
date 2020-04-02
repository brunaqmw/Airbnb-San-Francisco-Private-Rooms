# Airbnb-San-Francisco-Private-Rooms

Which neighborhood in San Francisco offers tourists private rooms that fit their budge, is safe, is close to Downtown and attractions? 

Let's find out what varibles can help us discover which neighborhood in San Francisco has the best(according to considerations above) private rooms to rent!

This research aims to help tourists decide which neighborhood in San Francisco has the best private rooms to rent. The
data was obtained from Kaggle, including 16 variables and 7833 observations. After data cleaning there are 7 variables and 2064 abservations.
Variables considered were: Neighborhood, Price, reviews_per_month, reviews_total, availability_365,  minimum_nights and calculated_host_listings_count.

Files included were: listings.xlsx, PrivateRooms.csv, PrivateRooms.xlsx, reviews.csv

Gathering necessary information from listings.xlsx...

There are 2885 private rooms. 

Private rooms' prices per night was decreased to $250 and now boxplot(privaterooms$price) has fewer outliers.
Boxplots were also created for minimum_nights, reviews_per_month, reviews_total, calculated_host_listings_count and availability_365.
After closely observing those boxplots, outliers were removed together as well as NA values.
Those boxplots now present a cleaner organization of the PrivateRooms.csv data.

Data frames were created for each variable except neighborhood which is the only categorical variable. A cleaned1.csv file was created with a data frame including all variables after cleaning their boxplots and reorganizing the data in a way all observations will match. Now we are left with 2064 observations.

The 35 Neighborhoods were abbreviated to a three-letter acronym, and then turned numerical by creating 10 subsets of neighborhoods, and they were saved under clean_sub.csv. Those subsets were then used to run tests against other variables. A barplot was created to analyze neighborhood subsets against price per private room. On this barplot you can observe that subset number 4(which includes: Mission(Mss), Potrero Hill(PtH), Castro Upper Market(C/M), Haight Ashbury(HgA)). 

Finally, a last_df1 dataframe was created with all 2064 observations and 8 variables including neighborhood subsets. File was saved under last_df1.csv file to further use to run tests with with each variable.

The first variables to be analyzed were Neigb_Sub and Price. 
A geom_jitter plot was created, and with this plot you can observe how most of the private rooms are under Neigb_Sub (4), were we also have the most expensive private rooms. 









