# data-512-project
#### Samuel Perebikovsky, sampereb@uw.edu

## Goal
The purpose of this project is to show how Florida's and specifically the County of Miami-Dade's reporting of COVID-19 data imapcts analysis and the how lack of transparency behind their reporting causes problems on scale ranging from individuals to the entire state. The project is the final assignment for the University of Washington DATA 512 A7. 


## Data Sources
- [Kaggle repository of Johns Hopkins University COVID-19 data](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv): Total number of COVID cases by day at the county level.
- [CDC Masking Mandate by State](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i): Mandatory masking mandate by state from the CDC.
- [The New York Times mask compliance survey data](https://github.com/nytimes/covid-19-data/tree/master/mask-use): Mask compliance data from a NYT survey
- [CDC Vaccination Data by County](https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh/data): Labor force and employment data


## Data Description


Here is a description of the final dataset (final_data_testing) after cleaning and processing.
|Column Name|Description|Data Type|Data Source|
|-|-|-|-|
|Year|the year of the data|Kaggle|
|Month|the month of the data|Kaggle|
|labor force|the number of people employed and looking for jobs|US Bureau of Labor Statistics|
|employment|the number of people employed|US Bureau of Labor Statistics|
|unemployment|the number of people unemployed|US Bureau of Labor Statistics|
|unemployment rate|the unemployment rate (unemployment/labor force)|US Bureau of Labor Statistics|
|time|the month end date|calculated from Year and Month|
|unemployment_diff|the change in unemployment from the previous month|calculated from US Bureau of Labor Statistics|
|labor_force_diff|the change in labor force from the previous month|calculated from US Bureau of Labor Statistics|
|covid_monthly_infection_diff|the change in new covid infection in each month|calculated from Kaggle|


## Known Issues
- My research produced counterintuitive results that unemployment rate and labor force granger caused covid infection rate. That is likely caused by the public policy in the US and a lack of more granular employment data.
- The imprecision in determining the number of close contacts limited my ability to draw any conclusion regarding the mask effectiveness.




## License and Terms of Use
- [Kaggle repository of Johns Hopkins University COVID-19 data](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv) is licnesed under Attribution 4.0 International (CC BY 4.0).
- [CDC Masking Mandate by State](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) is government-published data for public use.
- License for [The New York Times mask compliance survey data](https://github.com/nytimes/covid-19-data/tree/master/mask-use) can be found [here](https://github.com/nytimes/covid-19-data/blob/master/LICENSE). It allows for non-commercial use and requires credit to NYT. 
