# Final-Project-Tableau

## Project/Goals
The goal of the project is to working with data from the Canadian Open Data portal. The data is structured in the `data` folder as follow

- Weekly earnings from 1.1.2001 to 15.4.2015 (weekly_earnings - CSV, parsed from weekly_earnings.json)
- Housing constructions from 1955 to 2019 (real_estate_numbers - CSV)
- House prices from 1.1.2005 to 1.9.2020 (real_estate_prices - EXCEL)
- Housing_price_index from November 1979 to September 2020
- Office_realestate_index from November 1979 to September 2020
- Consumer index from November 1979 to September 2020

By analyzing the data to find the relationship between the consumer index and housing price index as well as making a prediction for the house price in the future
### Project structure
- data: contains the data sources
- presentation: contains the pdf file of the outcome story
- workbook: tableau workbook
- assignment.md: description about the tasks of the assignment
- README.md: overview about the project and tasks has been done as well as the outcome.
- data_visualisation.ipynb: to convert weekly earning from JSON to CSV
## Process
### Parsing the json to csv
Loading the json file and parsing it to csv in order for tableau can load as a data source.
### Answer the question
- Show the trend of house prices across Canada in the last 40 years (table housing_price_index).
  - According to the sheet `House Price Index`, the chart shows that the House Price index keeps going up over the last 40 years. It has some decrease at some years but overall is increasing.
- Compare the trend after 2005 with actual benchmark prices in table real_estate_prices to see if there are any differences.
  - According to the result in sheet `Housing Price Index vs Actual Benchmark`, it shows that the actual benchmark and the index are on the same trend. 
- Compare this trend with the trend of office prices. Which one is getting more expensive, faster?
  - The office price is going up too, even at higher percentage (182.8% compare to 155.4% of housing) as shown in the sheet `House Price vs Office`
- Create a heatmap of Canada with current house prices for each available district.
  - The heatmap of Canada with current house prices (the latest date is Sep, 2020) shows in the sheet `House Price Heat Map`
- Are the price differences between different districts increasing?
  - The price from difference district are increasing. As show in the sheet `House Price District`, the increasing in Edmonton is lower than Calgary, for example.
- Compare the trend of house prices with earnings. *In case you want to plot monthly salary, be aware that the earnings value is per week.
    - Even though the weekly salary earning keep increasing, the percentage of increase is still lower than the house price increase (45% compare to 63%) in the sheet `House Price vs Earnings`
- Did people spend more of their earnings in 2014 than they did in 2001?
    - No. The absolute value is higher but the percentage to their earning is the same. Considering the inflation, people actually do not spend more than they did in 2001 as shown in `Earnings vs Spendings`
- There were several economic crises in the world in the last 40 years, including these four: Black Monday (1987), Recession (early 1990s), dot com bubble (2000 - 2002), Financial crisis (2007 - 2009). Show the effect of these crises on:
  - Earnings
    - It actually had very slight impact to the earnings
  - House prices
    - The house prices drop in the recession and financial crisis but quickly recovered
  - Office prices
    - The office price drops in the recession and financial crisis but quickly recovered
  - House constructions
    - The House construcions drop very low during the recessions
  - Consumer index
    - The Black Monday doesn't show the impact. The Recession (early 1990s) impacted to the house price.
    - The dot com bubble (2000-2002) impacted to the consumer index and had a slightly impact to the house price index
- Plot consumer_index together with housing_price_index and fit the regression line between them. Can we predict consumer_index from the housing_price_index?
  - Because the R-squared is really high and the p-value is less than 0.05. We can say that we can predict the consumer index based on the housing price index
- Try to find an interesting pattern, trend, outlier, etc. from the data used in the above questions.
  - HINT : Double check all units in the table before any comparison.
## Results
An overview about the housing price and the earnings in Canada for over 40 years.
Even though that the earning is keep increasing, the house price has a bigger percentage of increase.

## Challenges 
The weekly earning is in JSON and it takes time to parse
There are some unit inconsistency, for example, the index value of consumer. It is hard to undertands because there is no information describing it.

## Future Goals
My question is if the population has played an important role to the housing price. I would like to find data related to the housing price and the population to find the gap between them.
