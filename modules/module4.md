# 4) Trend Analysis, Regression


```note
## Lab 4: Mann-Kendall and Multiple Linear Regression

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab: Regression](#)
  * data: [pillows_example.csv](data/pillows_example.csv)
* [Lab: Quantile Regression Modeling](#)
* [Lab: Confidence Intervals](#)

* [Lab 4-1: Mann-Kendall](lab4/lab4-1.ipynb)
  * data: [pillows_example.csv](data/pillows_example.csv)
* [Lab 4-2: Correlation, Multiple Linear Regression](lab4/lab4-2.ipynb)

```


## Homework 4

### Problem 1
 
Download the Dalles peak flow data.
 
USGS gaged streamflow records for the Columbia River at The Dalles, OR began in 1878 and continues to the present day (one of the longest continuous records in the U.S.). Peak flow records (based on peak stage values recorded by railroad workers), however, extend back even farther, to 1858. Using coincident peak flow records from 1879-1932 (a period with no major storage dams on the Columbia):

 **A.** First, isolate the period of relevant overlap (1879-1932) and plot the timeseries. Create a regression model for annual flow using spring peak flow as an explanatory variable.
 
 **B.** How much of the variance is explained by the resulting model?
 
 **C.** Estimate the 95% confidence bounds for the annual flow estimates from 1858- 1877, and plot them with the central tendency (the prediction from the regression model).
 
 **D.** Now create a non-parametric, quantile-based regression model using the same data.
 
 **E.** Plot the predictions and residuals for the two different prediction models for the training period (1879-1932) and plot the model predictions for the pre-1878 data for the two different models. Is there a substantial difference between the two model formulations?
 


### Problem 2

Download the datafile cascades_swe available here (.xlsx) or from the data folder on the class Canvas website (.xlsx or .mat). 

The data in the first three columns are values for total precipitation (mm), daily maximum temperature (°C ), and daily minimum temperature (°C) averaged from October-March over the Pacific Northwest Cascades in WA in OR. The fourth column is an estimate of April 1 snow water equivalent (in mm, the water content of the snowpack) from model simulations, averaged over the same domain.

 **A.** Calculate the long-term trend in April 1 SWE from 1916-2003 by fitting a linear model to the data. Estimate the uncertainty in the trend by evaluating a 95% confidence interval around the estimate of B1. That is:

Trend = X ± Y

 **B.** Is the trend statistically significant with 95% confidence? I.e. can we reject the null hypothesis that the trend is equal to zero?
    Repeat this analysis for only the more recent period 1950-2003.



### Problem 3:

Continue using the cascades_swe dataset for this problem. Begin by making scatterplots of each of these variables vs. all the other variables. One nice way to do this is as illustrated in Helsel and Hirsch Figure 2.39 on page 61 – this is not required, you can plot in whatever way works best for you.

 **A.** Calculate the correlation (R) between April 1 SWE and the three meteorological variables (precipitation, max. temperature and min. temperature), and also between all unique combinations of the meteorological variables.
 
 **B.** Calculate the autocorrelation in precipitation, maximum temperature and minimum temperature. Can we consider each of these values to be an independent sample? Or do some of them depend on the prior year’s sample?

```tip
In part **B**, we can test for autocorrelation at different lags, but not for any lag longer than a quarter of the length of the data series. Therefore, test for lags from 1 to N/4, where N is the length of the data series. Determine at which of these lags the autocorrelation is different than 0 with 95% confidence.
```

 **C.** Fit a multiple linear regression model to the data, using all three meteorological variables to predict April 1 SWE. Also calculate the trend in each meteorological variable. Estimate the overall trend in SWE, and trend due to each meteorological variable alone. How much of the overall trend is due to the combined effects of trends in both tmax and tmin?

 **D.** Finally carry out a Mann-Kendall test on the 1950-2003 April 1 SWE data. Is the trend significant according to this test? Compare your answer with your regression analysis for the same data in Problem 2B. **Note:** For this problem you do not need to worry about the tie statistic.






