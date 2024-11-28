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
 
   ![Screenshot 2024-11-27 at 12 39 59](https://github.com/user-attachments/assets/2cc4b9b4-3cbc-48cd-af8d-0839dcde26f8)

Version 2:
A team member raised concerns about data being in pivot-table-like format, vs more long format. Thus, having discovered flat files, I also employed a slightly different approach using 1) a flat txt data file (100MB) discovered working on the above, 2) the flat txt series file obtained in step 2 above, and 3) a txt file containing specific seriesid's of interest obtained similar to step 1 above (here, rather than download an xls file, I copy/pasted the seriesid's populated in the lower-left part of the screen into a txt file). Under this approach, the output is a single csv file, the series run from 2003-2023, focal activities are unchanged, and the script file is distinct. I do not reproduce the script file in the readme here in the interest of brevity. 

Note: footnote M in the data series = “Data collection issues in 2020 prevent the publication of 2020 annual, Q1, and Q2 ATUS estimates.”

### Major Sector Quarterly Labor Productivity and Costs
1. Download relevant flat files for all series from https://download.bls.gov/pub/time.series/pr/.
   
## Resources
* Series ID formats: https://www.bls.gov/help/hlpforma.htm
* ATUS footnotes: https://www.bls.gov/tus/footnote.htm
