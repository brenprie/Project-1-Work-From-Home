# Work From Home: Economic Impacts in the US

The Covid-19 pandemic pushed many to work from home (WFH), but as the health crisis has receded, a question that employers and employees alike have faced is whether to return to in-person work or whether to retain remote-work options. In this project, we seek to help inform this discussion by examining impacts of WFH using data available from the Bureau of Labor Statistics.

Potential questions we may be able to explore:
* Who works from home? Differences across industries, occuptions, and possibly gender pre-pandemic (2014 to 2018) vs post-pandemic (2019 to 2023). 
* How do changes in commute time pre- to post-pandemic translate to changes in time spent in other areas of one's life?
* How does WFH impact hours worked? 
* What is the productivity impact of WFH? How does the effect vary across industries and occupations? Are employees able to deliver similar/greater productivity while working fewer hours?
* Is remote work associated with a decrease employers’ labor costs, office rental costs, and/or utility costs? 

## Data: Series and Preparation

### American Time Use Survey

1. Download into xls multi-series table (2013-2023, annual) select time use statistics from https://www.bls.gov/tus/database.htm.
    1 -	gender:	Both sexes, Men, Women. 2 -	age group: all 10-year age bins and 18+. 3 - labor force status: All persons. 4 - select parents: All persons. 5 - activities: Select activities. 6 -	type of days: All days (weekday/weekend combined). 7 - type of estimate: Ave hours per day.
2. Download "flat" txt file (24MB) that contains series title. (Note: API pulls and pretty prints contained date and value fields but not series titles; series titles were discovered to reside in downloadable flat files.)
3. With assistance of ChatGPT, create and run script that reads xls and txt files, adds series title information to each worksheet in xls file based on series ID match, and saves output to both an updated xls file and csv files that correspond to each xls worksheet. 
 
   ![Screenshot 2024-11-27 at 12 39 59](https://github.com/user-attachments/assets/2cc4b9b4-3cbc-48cd-af8d-0839dcde26f8)

   
