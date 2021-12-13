# data-512-project
#### Samuel Perebikovsky, sampereb@uw.edu

## Goal
The purpose of this project is to show how Florida's and specifically the County of Miami-Dade's reporting of COVID-19 data imapcts analysis and the how lack of transparency behind their reporting causes problems on scale ranging from individuals to the entire state. We use both qualitative and quantitative analysis to paint a picture of just how messed up COVID data reporting is in Florida. The project is the final assignment for the University of Washington DATA 512 A7. 


## Data Sources
- [Kaggle repository of Johns Hopkins University COVID-19 data](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv): Total number of COVID cases by day at the county level.
- [CDC Masking Mandate by State](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i): Mandatory masking mandate by state from the CDC.
- [The New York Times mask compliance survey data](https://github.com/nytimes/covid-19-data/tree/master/mask-use): Mask compliance data from a NYT survey
- [CDC Vaccination Data by County](https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh/data): COVID-19 vaccination status by county from the CDC.
- [Miami-Dade Vaccinations by Zip Code](https://www.miamiherald.com/news/coronavirus/article254801602.html): COVID-19 vaccinations in Miami-Dade by Zip Code.


## Data Description

### Quantitative

Here is a description of the 2 final datasets (covidData1.csv, zipData2.csv) after cleaning and processing.

covidData1: merged data about covid vaccines, cases, and dates all at the county/state level (using CDC, Johns Hopkins)
|Column Name|Description|Data Type|
|-|-|-|
|Province_State|the state where the data came from (florida)|String|
|Admin2|the name of the county|String|
|Date|the date the data was collected|datetime|
|cases|total number of covid cases up the that date|int|
|NewCases|the number of covid cases reported that day|int|
|7dayAvg|the average number of cases reported per day in the last 7 days|double|
|day_of_week|the day that corresponds to the particular date|String|
|derivDiff|the rate of change of covid cases (infection rate)|double|
|7daySum|total number of covid cases reported in the last 7 days|int|
|FIPS|code corresponding to location in country|int|
|MMWR_week|morbidity and mortality weekly report|double|
|Recip_County|name of county that data belongs to|string|
|Series_Complete_Pop_Pct|The percentage of population that are fully vaccinated|double|
|Administered_Dose1_Pop_Pct|the percentage of population that has at least 1 dose of vaccine|double|
|Series_Complete_12PlusPop_Pct|percentage of population over 12 years old fully vaccinated| double|

zipData2: data about covid vaccinations at the zip code level (using Miami Herald)
|Column Name|Description|Data Type|
|-|-|-|
|ZCTA|zip code|int|
|percent_fullvax_eligible_DOH|percentage of population that are able to be vaccinated (Florida dept. of health)|double|
|percent_fullvax_total_DOH|percentage of population that are fully vaccinated (Florida dept. of health)|double|
|percent_fullvax_eligible_herald|percentage of population that are able to be vaccinated (Miami Herald est.)|double|
|%pop1dose|percent of population with at least one vaccine dose (calculated est.)|double|

- CDC [Dashboard](https://covid.cdc.gov/covid-data-tracker/#county-view)

For information on how the data was cleaned and filtered for this analysis please visit the A5/A6 jupyter notebook.

### Qualitative
- [Article 1](https://floridapolitics.com/archives/458515-miami-dade-90-vaccination-rate/)
- [Article 2](https://www.healthline.com/health-news/why-florida-now-has-the-lowest-covid-19-case-rate)
- [Article 3](https://www.tallahassee.com/story/news/local/state/2021/08/13/floridas-covid-numbers-cases-data-difficult-but-not-impossible-find-heres-how/8099274002/)
- [Article 4](https://www.wfla.com/community/health/coronavirus/lawsuit-filed-for-return-of-daily-covid-19-reports-in-florida/)
- [Article 5](https://www.miamiherald.com/news/coronavirus/article254801602.html)
- [Article 6](https://www.local10.com/news/local/2021/09/22/90-of-miami-dade-vaccinated-its-just-not-true-experts-say/)
- [Article 7](https://www.clickorlando.com/news/local/2020/11/26/florida-wont-release-covid-19-data-on-thanksgiving/)
- [Article 8](https://floridapolitics.com/archives/449831-florida-health-reports-impossible-vaccination-rates-withholds-confidential-covid-19-data-dems-say/)

All credit for the articles above should be given to the respective authors, without whom, this analysis would not be complete.

## Known Issues
- Much of the data from the Miami Herald are estimates of the true numbers since it was determined that the numbers by the department of health are not at all accurate.
- The Miami Herald article and data are past a paywall so you would need to subscribe or do a free trial to have access to it. However, there is a copy of the article and data in the repository.
- The qualitative data and articles may be biased.
- There are some blank/missing spots in the data.

## Process
To follow the process for this analysis please refer to project_A5_A6.ipynb for a guide on the quantitative side of the analysis. Supplement this with the articles linked above and you will be able to replicate my results and come to a similar conculsion.

## License and Terms of Use
- [Kaggle repository of Johns Hopkins University COVID-19 data](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv) is licnesed under Attribution 4.0 International (CC BY 4.0).
- [CDC Masking Mandate by State](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) is government-published data for public use.
- License for [The New York Times mask compliance survey data](https://github.com/nytimes/covid-19-data/tree/master/mask-use) can be found [here](https://github.com/nytimes/covid-19-data/blob/master/LICENSE). It allows for non-commercial use and requires credit to NYT. 
- [CDC vaccination data](https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh/data) is government-published data for public use.
