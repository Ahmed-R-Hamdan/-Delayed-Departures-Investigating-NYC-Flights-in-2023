## Understanding Flight Delays ✈️

Flight delays are a significant challenge for both the airline and passengers, causing disruptions, financial losses, and dissatisfaction.

Aanalyze historical flight data to uncover delay patterns, identify operational inefficiencies, and predict delays before they occur. By identifying delay patterns, predicting delays, and uncovering the factors that contribute most to delays.

These insights will help the airline make data-driven decisions to optimize scheduling, improve on-time performance, and enhance passenger satisfaction.

## 💾 The data

#### Your team provided you with 2 files with the following information ([source](https://www.kaggle.com/datasets/mahoora00135/flights/data)):

**flights.csv**
- `id` - Id number of the flight
- `year` - Year of Flight
- `month` - Month of Flight
- `day` - Day of Month
- `dep_time` - Time of departure (24h format)
- `sched_dep_time` - Scheduled departure time
- `dep_delay` - Delay in departure (minutes)
- `arr_time` - Time of arrival (24h format)
- `sched_arr_time` - Scheduled arrival time
- `arr_delay` - Delay in arrival (minutes)
- `carrier` - Airline company code  
- `flight` - Flight number 
- `tailnum`- Aircraft identifier number
- `origin` - Origin Airport - 3 letter code
- `dest` - Destination Airport - 3 letter code
- `air_time` - Duration of the flight (minutes)
- `distance` - Flight distance (miles)
- `hour` - Hour component of scheduled departure time
- `minute` - Minute component of scheduled departure time

**airlines_carrier_codes.csv**
- `Carrier Code` - Airline company code 
- `Airline Name` - Airline Name 



## 🎯 Key Finding

1. ✈️ Flight Delay Statistics – Insights from the Data

    - **61.15 %** of flights that experienced a departure delay also arrived late.
    - **15.37 %** of flights were delayed at departure but still managed to arrive on time.
    - **23.48 %** of flights that departed on time ended up arriving late.
    
So it's important to foucs on decreasing number of flights delayed at departure airport.

2.  🚨 **1.38%** of Flights Experienced Severe Delays (Over 3 Hours)

    - While this may seem like a small percentage, severe delays can result in significant financial losses, especially if the causes are attributable to airline-related issues such as operational inefficiencies, maintenance problems, or crew shortages.

    - These delays may trigger compensation obligations, increased passenger dissatisfaction, and disruption to the entire flight schedule, magnifying their impact across the network

3. **22.12%** of flights departing from NYC airports experienced delays, with the average delay lasting approximately 65 minutes.
4. Atlanta (ATL) is the top destination, receiving the highest number of flights **16,898** (flight each **31** minutes)
5. Out of **104** destination airports, **82** airports maintained a consistent schedule.The remaining **22** airports experienced irregular flight traffic.
6. **Hawaiian Airlines** operated **342** flights without any cancellations.
7. **ExpressJet Airlines** offers the widest coverage across the U.S. from New York City, serving 61 destinations. However, it also holds the highest cancellation rate among all carriers, with approximately **5.51%** of its flights—**2,817** out of **51,108**—being canceled.
8. Delayed and canceled flights Heatmap at 2023 shows
 - July experienced the highest delay rate at **30.19%** due to weather condition [source](https://www.cnbc.com/2023/06/30/july-fourth-holiday-flight-disruptions.html), while September saw the lowest delay rate at **14.29%**.
 - February had the highest cancellation rate at **15.28%**, whereas November had the lowest cancellation rate at **2.82%**.
 - High cancelation rate at February warrants further investigation, as no significant evidence of bad weather has been found to explain the spike

9. Based on your flight data, the GradientBoostingClassifier model can predict whether your flight will experience a departure delay, achieving an accuracy of **78.82%**.
