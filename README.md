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

Version 1: Excel-based. A team member raised concerns about data being in pivot-table-like format, vs more long format, so on to V2. 
 
Version 2:
1. Download flat data and series files from [https://download.bls.gov/pub/time.series/tu/](https://download.bls.gov/pub/time.series/tu/). Data file contains series title.
2. Obtain seriesid's of interest from [https://data.bls.gov/PDQWeb/tu](https://data.bls.gov/PDQWeb/tu). Copy/paste into txt file.
    1 -	gender:	Both sexes, Men, Women. 2 -	age group: all 10-year age bins and 18+. 3 - labor force status: All persons. 4 - select parents: All persons. 5 - activities: Select activities. 6 -	type of days: All days (weekday/weekend combined). 7 - type of estimate: Ave hours per day.
3. With assistance of ChatGPT, create and run script that reads files, spits series title into separate components, merges data, and generates a single csv file ready for data analysis. 

Version 2 Files ([Link to folder on repo](https://github.com/brenprie/Project-1-Work-From-Home/tree/brenprie/Raw%20Data/American%20Time%20Use%20Survey)):
* Input files: tu.data.1.AllData.txt, tu.series.txt, tu_select_series.txt
* Script file: fetch_bls_tu.ipynb
* Output file: tu_processed_data.csv
* Readme file: tu.readme.pdf

Version 2 Script:

![Screenshot 2024-11-28 at 00 17 17](https://github.com/user-attachments/assets/d93d53e0-1c05-44dd-9b3a-ef27317776b1)

Note: footnote M in the data series = “Data collection issues in 2020 prevent the publication of 2020 annual, Q1, and Q2 ATUS estimates.”

### Major Sector Quarterly Labor Productivity and Costs
1. Download relevant flat files (all series) from [https://download.bls.gov/pub/time.series/pr/](https://download.bls.gov/pub/time.series/pr/).
2. With assistance of ChatGPT, create and run script to read and merge files and save output to single csv file. Because series titles are not available in these files, obtain natural-English series identifiers by employing dictionaries that translate elements of the seriesid codes. I chose to define the dictionaries in-script, for ease and speed of delivering usable csv file; will modify script to read external dictionaries (more robust/flexible solution) later.  

Files ([Link to folder on repo](https://github.com/brenprie/Project-1-Work-From-Home/tree/main/Raw%20Data/Major%20Sector%20Quarterly%20Labor%20Productivity%20and%20Costs)):
* Input files: pr.data.1.AllData.txt, pr.series.txt
* Script file: fetch_bls_pr.ipynb
* Output file: pr_processed_data.csv
* Readme file: pr.readme.txt
* Series dictionaries: provided for perusal, but not treated as input files at this time

Script:

![Screenshot 2024-11-27 at 23 55 13](https://github.com/user-attachments/assets/cf8abdf2-a731-4fb7-ba43-e6344d282926)

Note: all series seasonally adjusted. 

### Major Sector and Major Industry Total Factor Productivity
1. Download flat files (all series) from [https://download.bls.gov/pub/time.series/mp/](https://download.bls.gov/pub/time.series/mp/).
2. With assistance of ChatGPT, create and run script to read and merge files and save output to single csv file. Series titles are available in these files, but rather than split the series titles into elements, I split series_ids into elements and mapped to natural-English identifiers by reading external dictionaries.  

Files ([Link to folder on repo](https://github.com/brenprie/Project-1-Work-From-Home/tree/main/Raw%20Data/Major%20Sector%20and%20Major%20Industry%20Total%20Factor%20Productivity%20(Annual))):
* Input files: mp.data.1.AllData.txt, mp.series.txt
* Script file: fetch_bls_mp.ipynb
* Output file: mp_processed_data.csv
* Readme file: mp.readme.txt
* Series dictionaries: in dictionaries folder

Script:

![Screenshot 2024-11-28 at 16 01 25](https://github.com/user-attachments/assets/b58aa481-914c-4f8c-8c25-55c6d1d524df)


## Resources
* Series ID formats: https://www.bls.gov/help/hlpforma.htm
* ATUS footnotes: https://www.bls.gov/tus/footnote.htm
