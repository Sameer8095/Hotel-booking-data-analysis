# Hotel-booking-data-analysis
data analysis of hotel booking
# Hotel Bookings Exploratory Data Analysis

## Objective
We are provided with a hotel bookings dataset. 

Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

## Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

```
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.
```

- Total number of rows in data: 119390
- Total number of columns: 32
## Data Cleaning and Feature Engineering

### (1) Removing Duplicate rows
All duplicate rows were dropped.

### (2) Handling null values
- Null values in columns `company` and `agent` were replaced by 0.
- Null values in column `country` were replaced by 'others'.
- Null values in column `children` were replaced by the mean of the column.

### (5) Creating new columns
- Created new column `total_stay` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
- Created new column `total_guest` by adding `adults`+`children`+`babies`.

## Exploratory Data Analysis

Performed EDA and tried answering the following questions:

```
 Q1) Which market segment makes the most no. of bookings?
 Q2) Which are the most busy months?
 Q3) From which country most of the guests are coming ?
 Q4) How long do people stay at the hotels?
 Q5)  Which year has most booking of hotels?
 Q6) Does a longer waiting period or longer lead time causes the cancellation of bookings?
 Q7) Which types of hotels are costly?

```

Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
  -  Bar Plot.
  -  Histogram.
   - Scatter Plot.
   - Pie Chart.
   - Line Plot.
   - Heatmap.

## Conclusion

1) The majority of the reservations are for city hotel than resort hotel and most in the year 2016.
2) The majority of the reservations are in the masoon and summer seasons
3) The guests are correlated with the adr which increases the revenue of the hotel
4) Most of the guests come from Portugal and other European countries.
5) Most of the Hotel Booking is done by online TA market segment and ofline TA/TO market segment.
6) Resort hotel prices are higher than the city hotel and most expensive in August and July.
7) Posibity of cancellation of booking increases with increase in lead time.
8) Most of guests prefer to stay in the hotel less than 5 nights

And many more conclusions.




