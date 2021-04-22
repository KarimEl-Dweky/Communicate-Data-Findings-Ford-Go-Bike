# Ford Go Bike Trip Data
## by Karim El-Dweky


## Dataset

> Bay Wheels is a regional public bicycle sharing system in California's San Francisco Bay Area. It is operated by Motivate in a partnership with the Metropolitan Transportation Commission and the Bay Area Air Quality Management District. Bay Wheels is the first regional and large-scale bicycle sharing system deployed in California and on the West Coast of the United States. It was established as Bay Area Bike Share in August 2013. As of January 2018, the Bay Wheels system had over 2,600 bicycles in 262 stations across San Francisco, East Bay and San Jose.

> In June 2017 the system was officially re-launched as Ford GoBike in a partnership with Ford Motor Company. After Motivate's acquisition by Lyft, the system was renamed to Bay Wheels in June 2019. The system is expected to expand to 7,000 bicycles around 540 stations in San Francisco, Oakland, Berkeley, Emeryville, and San Jose.

> The dataset used for this exploratory analysis consists of monthly individual trip data during February 2019 in CSV format contain approximately 183,412 rows.



> The structure of my dataset is 13 coloumns with 174,952 trip record. Each trip can be summarized in 4 categories:
   
>    - **Trip Duration Data:** [duration_sec, start_time, end_time, start_date, start_day, start_hour].
    - **Station Data:** [start_station_name, end_station_name]
    - **Bike Data:** [bike_id, bike_share_for_all_trip]
    - **Member Data:** [user_type, member_birth_year, member_gender, member_age]

> **The main features of interest are** the bike trips' duration and rental events occurrance patterns, along with how these relate to the members' characteristics, to get a sense of how and what people are using the bike sharing service for. 

> **Questions needs answer:**
    - When are most trips taken in terms of time of day or day of the week?
    - How long does the average trip take? 
    - Does the above depend on if a user is a subscriber or customer?
> **The features that will support my investigation are**
    - Trips Duration Data will help understanding how long a trip usually takes and when. 
    - Members Data like user type, gender and age will help us find out the main target customer groups, 
    - Using different type of data groups to summarize bike usage data to see if there is any special pattern associated with a specific group of members.



## Summary of Findings

> **Regarding Users, The service attracts more male users than female. Most members were Subscribers compared to Daily Customers. The majority of the members did not use bike share for all of their trips, and most were around 25 to 38 years old.**

> **The number of trips peaked around 8 am and 5 pm during a day, there were more trips on work days (Mon-Fri) compared to weekends.**

> **I cleand all variables that need to clean like change the date to datetime object,removed nan values, caclulated member age and removed the outliers.**

> **I've performed some operations on the data especially member age as the distribution shows that there were outliers should be cleaned, I've also changed a little bit in the structure of the data (data types and some drived coloumns) for ease of visualization and investigation.**



> **There are a lot more subscriber usage than customers. The Trip pattern norrow between subscribers and customers. Subscribers use the service for work commnute thus most trips were on work days (Mon-Fri) and especially during rush hours (when going to work in the morning and getting off work in the afternoon), whereas customers tend to ride for fun in the afternoon or early evenings over weekends.**

> **It is interesting to see that subscribers are slightly older than customers on average.**


> **The multivariate exploration strengthened some of the patterns discovered in the previous bivariate exploration as well as univariate exploration, the relationship between the multiple variables plotted are visualized altogether and information are presented combined. The efficient/short period of usage for subscribers corresponds to their high concentration on rush hours during working days, indicating the use is primarily for work commute. The more relaxing and flexible pattern of customer use shows that they're taking advantage of the service quite differently from the subscribers, heavily over weekends and in the afternoon, for city tour or leisure purpose probably.**

> **The Interesting finding was that females and others in gender are more enjoying the service than males and take more time in thier trips.**

## Key Insights for Presentation

> Subscribers contributed the majority of the usage, about 90%, while about 10% were consumed by cusomters. 
>Subscribers use the service for work commnute thus most trips were on work days (Mon-Fri) and at minimum in weekends, whereas customers tend to ride for fun so the trips count consider the same among the whole week.

> Males contributed the majority of the usage, about 74%, while about 24% were consumed by Females and about 2% by Others. 
>All Genders use the service for work commnute thus most trips were rush hours 8 am & 5 pm (when going to work in the morning and getting off work in the afternoon), However there is a percentage of  customers tend to ride for fun in the afternoon or early evenings.

> Males Users trips are much quicker compared to females & Others on each day of the week. For the latters The trip duration increases during weekends which means that Females and Others users are more likely enjoying the service more than just a ride.