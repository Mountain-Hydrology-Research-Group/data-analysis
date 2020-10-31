# 4) Trend Analysis, Regression


```note
## Lab 4: Regression and Trend Tests

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* Data: Annual peak snow water equivalent as measured at two snow-pillow sites [pillows_example.csv](data/pillows_example.csv) ([What is Snow Water Equivalent?](https://www.nrcs.usda.gov/wps/portal/nrcs/detail/null/?cid=nrcseprd1314833))
* [Lab 4-1: Linear Regression](lab4/lab4-1.ipynb)
* [Lab 4-2: Quantile Regression](lab4/lab4-2.ipynb)
* [Lab 4-3: Confidence Intervals](lab4/lab4-3.ipynb)
* [Lab 4-4: Mann-Kendall Trend Tests](lab4/lab4-4.ipynb)

```


## Homework 4

### Problem 1: Linear and Quantile Regression

Download the [streamflow records for the Columbia River](data/dalles_flow.csv)
 
USGS gaged streamflow records for the Columbia River at The Dalles, OR began in 1878 and continues to the present day (one of the longest continuous records in the U.S.). Peak flow records extend back to 1858 (based on peak stage values recorded by railroad workers). Using the coincident peak flow records from 1879-1932 (also a period with no major storage dams on the Columbia), create models to predict annual flow for years 1858-1877:

 **A.** Isolate the period of relevant overlap (1879-1932) and plot the timeseries. Create a linear regression model for annual flow using peak flow as an explanatory variable.
 
 **B.** How much of the variance is explained by the resulting model?
 
 **C.** Estimate the 95% confidence intervals for the annual flow predictions from 1858-1877, and plot them with the central tendency (the central tendency is the prediction from the regression model).
 
 **D.** Now create a non-parametric, quantile-based regression model using the same data.
 
 **E.** Plot the predictions and residuals for the two different prediction models for the training period (1879-1932), and plot the model predictions for the 1858-1877 data for the two different models. Is there a substantial difference between the two model formulations? Discuss any differences that you observe.
 


### Problem 2: Trend Analysis

Download the [cascades_swe.xlsx data file](data/cascades_swe.xlsx).

The first column is the water year, and data in the next three columns are values for total precipitation (mm), daily maximum temperature (°C), and daily minimum temperature (°C) averaged from October-March over the Pacific Northwest Cascades in Washington and Oregon. The last column is an estimate of April 1st snow water equivalent (in mm, the water content of the snowpack on this day) from model simulations, averaged over the same domain.

 **A.** Calculate the long-term trend in April 1 SWE from 1916-2003 by fitting a linear model to the data. Estimate the uncertainty in the trend by evaluating a 95% confidence interval around the estimate of B1. That is, report the trend as: 
$$
\hat{B}_1 \pm t_{\frac{\alpha}{2},n-2} \cdot s_{B_1} 
$$

 **B.** Is the trend statistically significant with 95% confidence? Can we reject the null hypothesis that the trend is equal to zero?

 **C.** Repeat this analysis (parts A and B) for just the more recent period, 1950-2003. Discuss any similarities or differences in the results of the two time periods.


### Problem 3: The best graphics
 
One of our greatest challenges in data analysis is to be able to visualize the information in the data and convey that information to others. Consider various scientific papers you have read (on any subject related to your scientific/engineering discipline) and pick out your favorite graphical representation of data (e.g., the best figure). Include your top two choices in your homework submission with a brief statement of why you chose these figures. We'll ask folks to share their favorites in class.