# Finding unusual Google search patterns for May 2020.
After installing necessary libraries, the Google search data is loaded in to a DataFrame from an online csv file.
Using loc create a new DataFrame for the month of May 2020.
Calculate the average search activity for May 2020 and for the entire period.  Then compare to see how May 2020 compares to the average.
The observation is that May 2020 search activity is 8.56% higher than the average.  Indicating that traffic increased after the announcement.

# Identify hourly, daily, and week of the year search patterns.
Use groupby and plot to show each.
Trend observations:
            1) starting ~9AM and peaks in the evening with highest traffic around midnight.
            2) Tuesday's are the busiest traffic day of the week.  Bulk of the traffic is Monday through Friday.  Weekends search trends are low.
            3) From a week of the year perspective, Q1 is the busiest search traffic period of the year.  Search seems to level off through middle of the year and drops significantly around week 35.  But then sales start to build again leading in to Q4 with highest periods (Q4) ~Nov and December--likely due to Black Friday/Cyber Monday and holiday sales taffic ramps.

# Combine search and stock data to find patterns.
Concatenate the search and stock DataFrames.  Then filter for Jan - Jun 2020.
Add 2 columns that hold stock volatility and hourly stock price change to evaluate correlation.
Trend observation is that there is weak/no correlation between lagged search data and stock volatility and price change.

# Create an 80-day forecast.
Create a Prophet() object.
Fit the DataFrame to the prophet object.
