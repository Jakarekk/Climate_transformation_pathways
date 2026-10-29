70% is a boundry:
          - indicator has less then 70% in a year in a specific country - that indicator in that year is going out
          - country has less then 70% data in setted time - it is going out

     * Indicator Energy Use has completely different structure - has much lower values. That's way a new boundry is set there - 65%

1990-2021 Based on data (year_completeness section) - the dataset has to be coherent

Check other completness boundries ??!!!

# WORLD DEVELOPMENT INDICATORS


     - Country & Economy - uploaded the official list of countries from WDI and deleted everything beyond that list.

     - Series: 
          - 'Total greenhouse gas emissions excluding LULUCF per capita (t CO2e/capita)',
          - 'Carbon intensity of GDP (kg CO2e per constant 2015 US$ of GDP)',
          - 'Energy intensity level of primary energy (MJ/$2021 PPP GDP)',
          - 'Renewable energy consumption (% of total final energy consumption)',
          - 'Energy use (kg of oil equivalent per capita)',
          - 'GDP per capita (constant 2015 US$)'

     
     Energy intensity has values since year 2000 - the serie will be removed and the value will be calulated manually.

     0 that are correct (true zeros, kept as is):
          - Gulf states (Bahrain, Saudi Arabia, Oman, Kuwait, Qatar, UAE) - no hydro, no biomass, energy system based on oil and gas, first large solar installations only after ~2018
          - Malta - in fact there wasn't any renewable sources then (leading zeros 1990-2001)
          - Turkmenistan - gas industry (leading zeros 1990-1997)
          - Hong Kong - negligible renewable share, single zero in 2000 = rounding (<0.005%)

     0 that are NOT correct:
          - Turkmenistan 2012 - interpolate!!!!
          - Namibia 1990 (Energy use) - the country was created that year 

     Nans:
          There are gaps on the edges in Laos, Jemen, Cambodia - despite over 70% completeness they need to be removed due to unstable version of interpolation - on the edge. 


# Eurostat

## Demo_pjan - DEMOGRAPHY

Freq
Unit
Age
Sex
Geo\\TIME   - Names of countries
               - There are some longer names - they are some groups of countres like Europe or European Industrial Area - gonna get rid of it as it overcome just single countries
               - German!!!! - I will continue with DE_TOT - it seems that DE does not contain whole popularity during split of Germany and in the recent years the population is the same.  
                (Split of Germany - 1949 - 1990)
               - FRANCE!!!! - FR from 1991
                              FX to 2013 (excluded) - European and others
                              Solution:
                                   FR is the main dataset years without data are filled with FX data 


            Thats it. Switching to WDI.


Values:
     - There are some values with Eurostat's terminology - created another column for that, maybe to consider in the future.

     

