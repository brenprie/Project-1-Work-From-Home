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

Version 1:
1. Download into xls multi-series table (2013-2023, annual) select time-use data from [https://data.bls.gov/PDQWeb/tu](https://data.bls.gov/PDQWeb/tu).
    1 -	gender:	Both sexes, Men, Women. 2 -	age group: all 10-year age bins and 18+. 3 - labor force status: All persons. 4 - select parents: All persons. 5 - activities: Select activities. 6 -	type of days: All days (weekday/weekend combined). 7 - type of estimate: Ave hours per day.
2. Download "flat" series file (24MB) from [https://download.bls.gov/pub/time.series/tu/](https://download.bls.gov/pub/time.series/tu/), which contains series title. (Note: API pulls and pretty prints contained date and value fields but not series titles; series titles were discovered via search to reside in downloadable flat files.)
3. With assistance of ChatGPT, create and run script that reads xls and txt files, adds series title information to each worksheet in xls file based on series ID match, and saves output to both an updated xls file and csv files that correspond to each xls worksheet. 
 
Version 2:
A team member raised concerns about data being in pivot-table-like format, vs more long format. Thus, having discovered flat files in the prior version, I next employed a different approach using 1) a flat txt data file (100MB) downloaded from the link in step 2 above, 2) the flat txt series file obtained in step 2 above, and 3) a txt file containing the select seriesid's of interest (here, I copy/pasted the seriesid's listed in the bottom of the screen into a txt file). Under this implementation, the output is a single csv file and the series run from 2003 to 2023; the focal activities are unchanged relative to v1. 

Version 2 Files:
* Input files: tu.data.1.AllData.txt, tu.series.txt, tu_select_series.txt
* Script file: fetch_bls_time_use.ipynb
* Output file: tu_processed_data.csv
* Readme file: tu.readme.pdf

Version 2 Script:

![Screenshot 2024-11-28 at 00 17 17](https://github.com/user-attachments/assets/d93d53e0-1c05-44dd-9b3a-ef27317776b1)

Note: footnote M in the data series = “Data collection issues in 2020 prevent the publication of 2020 annual, Q1, and Q2 ATUS estimates.”

### Major Sector Quarterly Labor Productivity and Costs
1. Download relevant flat files for all series from https://download.bls.gov/pub/time.series/pr/.
2. Because series titles are not available in the downloads, obtain natural-English series identifiers by employing dictionaries that translate relevant elements of the seriesid codes. I chose to define the dictionaries in-script rather than read the external dictionary files for ease and speed of delivering usable data files to the team. Reading external files would have the additional benefit of greater scalability, or flexibility if dictionaries are subject to change, and would also allow for ease of use across scripts/projects. Note: I dropped some columns not be relevant for this project (e.g., series start- and end-year information) to reduce file size somewhat.  

Files:
* Input files: pr.data.1.AllData.txt, pr.series.txt
* Script file: fetch_bls_productivity_costs.ipynb
* Output file: pr_processed_data.csv
* Readme file: pr.readme.txt
* Series dictionaries: provided for perusal, but not treated as input files at this time

Script:

![Screenshot 2024-11-27 at 23 55 13](https://github.com/user-attachments/assets/cf8abdf2-a731-4fb7-ba43-e6344d282926)

Note: all series seasonally adjusted. 

### Major Sector and Major Industry Total Factor Productivity
-coming soon-

## Resources
* Series ID formats: https://www.bls.gov/help/hlpforma.htm
* ATUS footnotes: https://www.bls.gov/tus/footnote.htm
