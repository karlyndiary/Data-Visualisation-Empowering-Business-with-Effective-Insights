## Here is the background information on your task

The CEO and CMO have recently met to finalise the requirements and would like you to provide them with some analysis and visuals that would help answer their questions. Both, the executives are interested in viewing and understanding how they can use the data to make more meaningful decisions. You would need to provide insights which they can use to create the expansion strategy. The executives want to analyse the trends and the breakdown by different categories so that they have clarity on how the revenue is being generated and what are the main factors affecting the online store.

You will be provided with the requirements of the executives and how they want to view the data. After the requirement gathering phase, you would need to make sure that the data you are using is of good quality and does not contain any bad data that would have an adverse impact on your analysis. Once the data is cleaned, the next step would be to create the visuals on either Tableau or Power BI. No matter which tool you choose for the visuals, the result should be the same. These results will help the executives with effective decision making and assist in their expansion strategy.

### Questions

#### Question 1
The CEO of the retail store is interested to view the time series of the revenue data for the year 2011 only. He would like to view granular data by looking into revenue for each month. The CEO is interested in viewing the seasonal trends and wants to dig deeper into why these trends occur. This analysis will be helpful for the CEO to forecast for the next year.

#### Question 2
The CMO is interested in viewing the top 10 countries which are generating the highest revenue. Additionally, the CMO is also interested in viewing the quantity sold along with the revenue generated. The CMO does not want to have the United Kingdom in this visual.

#### Question 3
The CMO of the online retail store wants to view the information on the top 10 customers by revenue. He is interested in a visual that shows the greatest revenue generating customer at the start and gradually declines to the lower revenue generating customers. The CMO wants to target the higher revenue generating customers and ensure that they remain satisfied with their products.

#### Question 4
The CEO is looking to gain insights on the demand for their products. He wants to look at all countries and see which regions have the greatest demand for their products. Once the CEO gets an idea of the regions that have high demand, he will initiate an expansion strategy which will allow the company to target these areas and generate more business from these regions. He wants to view the entire data on a single view without the need to scroll or hover over the data points to identify the demand. There is no need to show data for the United Kingdom as the CEO is more interested in viewing the countries that have expansion opportunities.


### Data Cleaning

- The quantity should not be below 1 unit
```
Filter set to - At least 1
```

- The Unit price should not be below $0
```
Filter set to - At least 0
```

- Revenue
```
[Unit Price]*[Quantity]
```

- Min/Max Revenue
```
IF SUM([Revenue]) = WINDOW_MAX(SUM([Revenue]))
THEN SUM([Revenue])
ELSEIF SUM([Revenue]) = WINDOW_MIN(SUM([Revenue]))
THEN SUM([Revenue])
END
```
