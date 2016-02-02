# Stock-Predictor-Application

##Introduction
This app uses lets you pick which public company to perform a regression analysis on, and lets you choose which predictors (financial ratios) you would like to include in the stock price prediction. This app also compares different ratios and view various financial data of your selected company. **Click this link to go to the web application stock predictor:** [**Click Here!!**](https://jnacino.shinyapps.io/Stock-Predictor-Application/)



##Method

Using R software I was able to clean and merge multiple datasets. I extracted data from the following sources: 

1. **quantmod** package (R package)
2. **http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=nasdaq&render=download** (csv file)
3. **http://www.nasdaq.com/screening/companies-by-name.aspx?letter=0&exchange=nyse&render=download** (csv file)

Using the Shiny package I constructed the web application in which a person would have various predictors (financial ratios) to choose from when wanting to make a price prediction for their selected stock. Stock price is the response (dependent) variable in this appliction. The time variable **Date** is always selected as an explanatory (independent) variable during each analysis. The following explanatory variables are up to the user to select:

**Predictors** 

1. Return on Assets
2. Return on Equity
3. Profit Margin
4. Current Ratio
5. Quick Ratio
6. Debt to Euity Ratio
7. Tnterest Coverage Ratio
8. Asset Turnover Ratio
9. Inventory Turnover Ratio

For more info about the ratios, go to this site: [**Click Here!!**](http://www.investinganswers.com/education/ratio-analysis/15-financial-ratios-every-investor-should-use-3011)

##Testing

Using the web application that I made, [**Link**](https://jnacino.shinyapps.io/Stock-Predictor-Application/), I was able to test the various financial ratios and their correlation to stock price. 

When running the linear model analysis through R software, it reports many values. The three values that are very signifcant in the report is the p-value, the R-Squared value (shown as multiple R-squared in the web app), and adjusted R-Squared.  The p-value tells the significance of the model. A p-value less than .05 means that the linear model is indeed significant. For example, if I had a p-value of .04, this means that there is a 96% probability (100% - 4%) that the slope of the linear model is not zero. Note, that if the slope is zero, then an increase in our predictor variable does not affect on the response variable. The R-squared value is used to determine the accuracy that our linear model will predict. the closer the R-squared value is to 1, the more accurate the predictions will be as an R-squared value of 1 means a perfect linear fit of the data set. The adjusted R-Squared is useful in multi-variable regression analyis (adding multiple predictors) because if the adjusted R-Squared has increased with an addition of an extra variable, then it would mean that the prediction should be more accurate. 

I tested a regression model through 30 days and 120 days of historic stock prices, and a regression model through historic stock prices which includes data all the way from when the company issued their quarterly balance sheet five quarters ago to the last market close.


##Results and Conclusion

It is not easy to predict the price of a stock. Many variables besides financial ratios affect the price of a stock such as the CEO stepping down or an unpredictable DISASTER. I would have to test more companys' stock on this predictor and track the results to conclude whether or not this predictor can predict with accuracy. 
