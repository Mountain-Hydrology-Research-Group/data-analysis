# Week 4


```note
## Lab 4: Mann-Kendall and Multiple Linear Regression

Download the lab file to the same folder you created in Lab 1.0. Then, open the lab file using Jupyter Notebook and follow the directions.

 * Lab 4.1 (.ipynb) Mann-Kendall [preview]
   * data: pillows_example.csv
 * Lab 4.2 (.ipynb) Correlation, Multiple Linear Regression lab?

```


## Homework 4

### Problem 1

Download the datafile cascades_swe available here (.xlsx) or from the data folder on the class Canvas website (.xlsx or .mat). 

The data in the first three columns are values for total precipitation (mm), daily maximum temperature (°C ), and daily minimum temperature (°C) averaged from October-March over the Pacific Northwest Cascades in WA in OR. The fourth column is an estimate of April 1 snow water equivalent (in mm, the water content of the snowpack) from model simulations, averaged over the same domain.

 **A.** Calculate the long-term trend in April 1 SWE from 1916-2003 by fitting a linear model to the data. Estimate the uncertainty in the trend by evaluating a 95% confidence interval around the estimate of B1. That is:

Trend = X ± Y

 **B.** Is the trend statistically significant with 95% confidence? I.e. can we reject the null hypothesis that the trend is equal to zero?
    Repeat this analysis for only the more recent period 1950-2003.



### Problem 2:

Continue using the cascades_swe dataset for this problem. Begin by making scatterplots of each of these variables vs. all the other variables. One nice way to do this is as illustrated in Helsel and Hirsch Figure 2.39 on page 61 – this is not required, you can plot in whatever way works best for you.

 **A.** Calculate the correlation (R) between April 1 SWE and the three meteorological variables (precipitation, max. temperature and min. temperature), and also between all unique combinations of the meteorological variables.
 
 **B.** Calculate the autocorrelation in precipitation, maximum temperature and minimum temperature. Can we consider each of these values to be an independent sample? Or do some of them depend on the prior year’s sample?

```tip
In part **B**, we can test for autocorrelation at different lags, but not for any lag longer than a quarter of the length of the data series. Therefore, test for lags from 1 to N/4, where N is the length of the data series. Determine at which of these lags the autocorrelation is different than 0 with 95% confidence.
```

 **C.** Fit a multiple linear regression model to the data, using all three meteorological variables to predict April 1 SWE. Also calculate the trend in each meteorological variable. Estimate the overall trend in SWE, and trend due to each meteorological variable alone. How much of the overall trend is due to the combined effects of trends in both tmax and tmin?

 **D.** Finally carry out a Mann-Kendall test on the 1950-2003 April 1 SWE data. Is the trend significant according to this test? Compare your answer with your regression analysis for the same data in Problem 2B. **Note:** For this problem you do not need to worry about the tie statistic.






