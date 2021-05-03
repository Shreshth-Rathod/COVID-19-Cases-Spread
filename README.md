# Exploring COVID-19 Cases & Spread in R

# Introduction

- Coronavirus, also known as COVID-19, is a serious illness, caused by a contagious virus. It quickly spreads via contaminated surface-to-person contact and person-to-person contact. It has considered as a pandemic as it has spread over multiple countries or continents and has affected numerous people in multiple different ways.

- This infectious disease falls under respiratory disease. Symptoms observed amongst the infected people are in wide range which include mild fever to severe illness. It has caused numerous hospitalizations and deaths globally and particularly in the U.S.

- Researchers around the world have created models to predict the trajectory of COVID-19. Models are not always perfect in making predictions, but they may be substantially useful if applied correctly3. In case of COVID-19 responding to these models may be the difference between death tolls in the thousands or millions4. On the basis of existing prediction models for COVID-19, CDC recommends the public to wear face masks in places with high population density because it is difficult to maintain social distancing or 6 feet distance1.

# Contents

- [The Data Set](#the-data-set)
  - [Data Selection](#data-selection)
  - [Data Wrangling](#data-wrangling)
  - [Geographic Exceptions for COVID Cases](#geographic-exceptions-for-covid-cases)
  - [Exclusion Criteria](#exclusion-criteria)
- [Used Tools](#used-tools)
- [Conclusion](#conclusion)
- [Follow Me On](#follow-me-on)


# The Data Set
### Data Selection
  - COVID-19 cases for county level was obtained from the New York Times and GitHub database. 

    - State level variables include 
      - Top 50 Populated U.S. city 
      - Top 50 walkable U.S. city
      - Top 50 public transit U.S. city 

    - County level explanatory variables were obtained from USDA-ERS. 
      - Number of households
      - Population
      - Population density
      - County classification

### Data Wrangling
  - USDA dataset was downloaded in the initial stage, after manipulating the dataset in excel, columns taken into consideration were: 
    - Number of households 
    - Population 
    - Population density 
    - County classification 
  - Total population, number of household and population density data were present in single excel file. 
  - County classification column was present in another excel file. 
  - GitHub-County level cases data was present in another excel file. 
  - These files were merged on FIPS code.
  - State level exploratory variables were taken into consideration for further exploration of data. Hence, they were merged on State.
 
### Geographic Exceptions for COVID Cases
  - Cases for 5 NYC counties are reported as just NYC. 
  - We changed explanatory variables accordingly: 
    - NYC households = sum households of 5 NYC counties 
    - NYC population = sum population of 5 NYC counties 
    - NYC population density = sum population of 5 NYC counties / sum area of 5 NYC counties 
  - Cases for Kansas City, MO were not reported at county-level. 
  - Cases for Alameda County, CA include Berkeley and the Grand Princess cruise ship. 

### Exclusion Criteria
- We removed 23 states that has less than 5000 total COVID-19 cases on 04/24/20. We removed counties with less than 5 COVID-19 cases. Thus, 77.3% (1540/1992) of counties were included in the analysis. 


# Used Tools
- Rstudio


# Conclusion
- The results from this exploratory data analysis show that greater number of households, population size, population density leads to greater COVID-19 cases and faster COVID-19 spread. Metro counties have greater COVID-19 cases and faster COVID-19 spread than Nonmetro counties. NY state and NY county have the greatest cases and fastest spread for COVID-19. Therefore, the number of households, population size, population density and county classification contributed to the enormous COVID-19 cases spread. As population density increases, social distancing can be difficult. This may have led CDC to update recommendation about wearing face masks in public places on April 13th.


# Follow Me On
http://linkedin.com/in/shreshthrathod
