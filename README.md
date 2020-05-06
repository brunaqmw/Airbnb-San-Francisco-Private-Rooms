# Airbnb-San-Francisco-Private-Rooms

Which neighborhoods in San Francisco offer tourists private rooms that fit their budget, are safe (crime-wise), close to Downtown and attractions?

Let's find out what variables can help us discover which neighborhoods in San Francisco have the best (according to considerations above) private rooms to rent!

This research aims to help tourists decide where their ideal locality will be  in “The Golden City”.


PHASE 1 OF ANALYSIS:

The data was obtained from Kaggle, including 16 variables and 7833 observations. After data cleaning there are 7 variables and 2064 observations.
Variables considered were: Neighborhood, Price, reviews_per_month, reviews_total, availability_365,  minimum_nights and calculated_host_listings_count.

Files first included:

Listings.xlsx- where all listings for Airbnbs in San Francisco are found. Including details like: number_id of listing, name, host_name, neighborhood, room_type, price, and many more interesting features.   

PrivateRooms.csv- which includes all Airbnbs private rooms from listings. Including all details above.

Reviews.csv-  includes listing_id and date of reviews.

Gathering necessary information from listings.xlsx…

There are 2885 private rooms. Private rooms' prices per night were decreased to $250 and now boxplot(privaterooms$price) has fewer outliers. ADD BOXPLOT LINE#120

Boxplots were also created for minimum_nights, reviews_per_month, reviews_total, calculated_host_listings_count and availability_365.
After closely observing those boxplots, outliers were removed as well as NA values.
Those boxplots now present a cleaner organization of the PrivateRooms.csv data.

Data frames were created for each variable including neighborhood. TRY TO ADD DATAFRAME

 A cleaned1.csv file was created with a data frame including all variables after cleaning their boxplots and reorganizing the data in a way all observations would match. The 35 Neighborhoods were abbreviated to a three-letter acronym, and now we are left with 2064 observations. ADD BOXPLOT LINE#449-455

Those neighborhoods were then turned numerical to run tests against other variables. Subsequently, stored in 10 categorical subsets. Those subsets were created based on proximity to neighborhoods, saved under clean_sub.csv.

A barplot of “clean_sub” was created to analyze neighborhood subsets against price per private room. On this barplot it can observed that subset number 4(which includes: Mission(Mss), Potrero Hill(PtH), Castro Upper Market(C/M), Haight Ashbury(HgA)), with 455 private rooms available has the greatest price change per room, with maximum price being over $400. Hence, after merging these neighborhoods together from decreased $250 price per night, per neighborhood, there’s an increase of $150 when considering subsets of neighborhoods.  ADD BARPLOT LINE#414

Another data frame was created named last_df1. Containing all 2064 observations with 8 variables including neighborhood subsets and neighborhoods acronyms. With this data frame further analysis can be made. The first variables to be analyzed were Neigb_Sub and Price.
ADD PLOTS LINE#517


RESULT OF FIRST ANALYSIS:

After analysing box plots, barplots, geom_jitter etc, for price against neighborhoods then price against neighborhood-subsets, results show that neighborhood subset #2- Marina(Mrn), North Beach(NrB), Russian Hill(RsH), with 77 private rooms has the highest price per subset. Perhaps, because it has the least amount of private rooms per subset?
Further analysis will explain the price of those subsets when it comes to how safe they are, and how close they are to famous attractions. Let’s find out!


PHASE 2 OF ANALYSIS:

Subsets of neighborhoods were examined in regards to how safe they were. Afterwards, a numerical safe subset was created, subsetted into 5 different categories: (1-2)-highest safety, (3-4)- high safety, (5-6)- low safety, (7,8)- lower safety, and lastly (9,10)- lowest safety. Safety was based on the rate of annual crime, violent crimes and property theft reports for 2019.

Plots created:

The first plot was a geometric jitter plot, with level of safety(cat_sub) against safe subsets(safe_sub).
ADD PLOT #723 and add explanation

A Lollipop plot was created, including the first neighborhood subset, which resulted in having subset  (2)- Marina(Mrn), North Beach(NrB), Russian Hill(RsH), with 77 private rooms having the highest price per subset, and the safe_sub. That same subset number (2) ended up being number (9) when it comes to safety. Meaning that, for the data in this plot, price does not depend on safety. In addition, a box plot of safe_sub against price was created. ADD PLOTS LINE#740, 768


RESULT OF SECOND ANALYSIS:

Above it can be seen that the box plot supports the evidence presented with the Lollipop plot, that safe_sub number (9) having the lowest safety, and the least amount of rooms, is the most expensive subset. Therefore, safety level of neighborhood subsets is not the main criteria involved when selecting which airbnb private room to rent in San Francisco.


PHASE 3 OF ANALYSIS:

How much does being close to attractions affect the price of private rooms? 

For phase number three of the analysis, the focus is on finding out which neighborhood subset is closer to famous attractions. And if whether or not the fact of being closer to those attractions changes the price of private rooms to rent. 

The same subset of neighborhoods first created was used to create new subsets of neighborhoods close to attractions from (1-10). Which was then turned into a subset(cat_sub) where: (1-2) is nearest to famous attractions, (3-4) is nearer, (5-6) near, (7-8) further and (9-10) furthest from famous attractions. 

Plots created to analyse safe_sub with proximity to attractions subset where: a geom_point and geom_jitter: ADD PLOTS LINE#961

#Above shows safe_subs and how close they are to most famous attractions.
# Subset of safe_sub (1) - Crocker Amazon, Ocean View and Outer Mission,  is further from famous attractions,  and safe_sub (9) - Marina, North Beach, Russian Hill is nearest to the most famous attractions. 



