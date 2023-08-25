# Homework 4

## Problem 1: ANOVA

This problem is based on material in Lab 3-2.

Download the [HJ Andrews Peak Flow data](/data/HJAndrews_peakflow_WS1_WS2_WS3.xlsx).

For this problem, consider only differences between watershed 1 (WS1) and watershed 2 (WS2). These two watersheds are adjacent to each other in the [HJ Andrews Experimental Forest](https://andrewsforest.oregonstate.edu/). We want to test if there was a change in streamflow due to the forest within WS1 being completely clearcut (starting late 1962 and completed in 1966). Because the two watersheds are adjacent, we can expect that they experience the same storms leading to peak runoff (so we won't be considering any differences due to different precipitation amounts or timing). 

Here we want to test whether the difference in peak flows between WS1 and WS2 is statistically different for four different time periods:

| Time Period | Years | Label | Notes |
| ----------- | --------------- | --------------- | --------------- |
| control period | 1953-1962 | 1 | before any clearcutting in WS1 |
| active clearcutting | 1963-1966 | 2 | during clearcutting of WS1 |
| 0-15 years after clearcutting | 1967-1981 | 3 | WS1 forest starts to recover |
| >15 years after clearcutting | 1982-2015 | 4 | WS1 forest recovering further |

The field "Index12" identifies our two different treatments as either 1 or 2.

We want to know whether the four periods are statistically different from each other, and if so, which one or ones are statistically different from which other ones.

 **A.** First, plot the timeseries of the streamflow measurements as a function of water year for both watershed 1 and watershed 2 on the same graph. Use vertical dashed lines ([axvline in matplotlib](https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.axvline.html)) to indicate the different periods (put a vertical dashed line in 1963, in 1967, and in 1982).
 
 **B.** It has been suggested that paired data such as this can be made to be closer to normally distributed by taking the log of each value before subtracting. Create two datasets: `Q12 = streamflow1 - streamflow2` and `Qlog12 = log(streamflow1)- log(streamflow2)` and make graphs to demonstrate which is closer to normally distributed. Given that we want to use an ANOVA analysis, explain why is it important to do a transformation to get the data closer to normally distributed?
 
 **C.** State the null and the alternative hypothesis for the question of whether the four periods are statistically different from each other. State the type I error (alpha value) that you are willing to accept.
 
 **D.** Perform an ANOVA test and discuss the results, related both to your hypothesis test listed above and to the more detailed question of which groups are statistically different from which other groups. Include graphs and/or tables that illustrate your results, and be sure to discuss what they mean. When using these ANOVA and other statistics functions, be sure that you understand what the code is doing (especially the defaults that different functions use) and outputting.
 

## Problem 2: Linear and Quantile Regression

Download the [streamflow records for the Columbia River](/data/dalles_flow.csv)
 
USGS gaged streamflow records for the Columbia River at The Dalles, OR began in water year 1879 and continues to the present day (one of the longest continuous records in the U.S.). Peak flow records extend back to 1858 (based on peak stage values recorded by railroad workers). Using the coincident peak flow records from 1879-1933 (also a period with no major storage dams on the Columbia), create models to predict annual flow for years 1858-1878:

 **A.** Isolate the period of relevant overlap (1879-1933) and plot the timeseries. Create a linear regression model for annual flow using peak flow as an explanatory variable.
 
 **B.** How much of the variance is explained by the resulting model?
 
 **C.** Estimate the 95% confidence intervals for the annual flow predictions from 1858-1878, and plot them as a timeseries (estimates each year) with the central tendency (the central tendency is the prediction from the regression model).
 
 **D.** Now create a non-parametric, quantile-based regression model using the same data.
 
 **E.** Plot the predictions and residuals for the two different prediction models for the training period (1879-1933), and plot the model predictions for the 1858-1878 data for the two different models. Is there a substantial difference between the two model formulations? Discuss any differences that you observe.
 


## Problem 3: Trend Analysis

Download the [cascades_swe.xlsx data file](/data/cascades_swe.xlsx).

The first column is the water year, and data in the next three columns are values for total precipitation (mm), daily maximum temperature (°C), and daily minimum temperature (°C) averaged from October-March over the Pacific Northwest Cascades in Washington and Oregon. The last column is an estimate of April 1st snow water equivalent (in mm, the water content of the snowpack on this day) from model simulations, averaged over the same domain.

 **A.** Calculate the long-term trend in April 1 SWE from 1916-2003 by fitting a linear model to the data. Estimate the uncertainty in the trend by evaluating a 95% confidence interval around the estimate of B1. That is, report the trend as: Trend = B1 ± t*sB1


 **B.** Is the trend statistically significant with 95% confidence? Can we reject the null hypothesis that the trend is equal to zero?

 **C.** Repeat this analysis (parts A and B) for just the more recent period, 1976-2003. Discuss any similarities or differences in the results of the two time periods.



## Problem 4: Project (CEWA 565)

Please give a brief update of where you are with your project.  At this poing you should have acquired data that you can plot.  Include one example plot of the data in this homework.  Let us know if you have any questions or concerns at this point.