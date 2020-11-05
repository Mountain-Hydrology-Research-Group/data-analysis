# 5) Regression, Data Visualization

```note
## Lab 5: Multiple Linear Regression & Autocorrelation

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

Data visualization:
* [Interactive Plots](lab5/interactive-plots.ipynb) with [iButtons_2008-2010.mat](data/iButtons_2008-2010.mat)
* [Warming Stripes Figure](lab5/warming-stripes.ipynb)

Multiple Linear Regression & Autocorrelation:
* [Lab 5-1: Multiple Linear Regression](lab5/lab5-1.ipynb) with [pillows_example.csv](data/pillows_example.csv)
* [Lab 5-2: Autocorrelation](lab5/lab5-2.ipynb) with [iButtons_2008-2010.mat](data/iButtons_2008-2010.mat)

```

## Homework 5

### Problem 1: Correlation, Autocorrelation, Multiple Linear Regression

In this problem, you will explore the relationship between air temperature, precipitation, and [snow water equivalent](https://www.nrcs.usda.gov/wps/portal/nrcs/detail/null/?cid=nrcseprd1314833) over time, using observations from a study site in the Washington Cascades. Download the [cascades_swe.xlsx](data/cascades_swe.xlsx) dataset for this problem.

**A.** Begin by making scatterplots of each of these variables vs. all the other variables. Describe any visual patterns you see between each pair of variables.

**B.** Calculate the correlation (R) between April 1 SWE and the three meteorological variables (precipitation, maximum temperature, and minimum temperature). Then also calculate R between each unique combination of the meteorological variables. 
 
**C.** Calculate the autocorrelation in precipitation, maximum temperature, and minimum temperature over the timeseries. Can we consider each of these values to be an independent sample? Or do some of them depend on the prior year’s sample?

```tip
In part **C**, we can test for autocorrelation at different lags, but not for any lag longer than a quarter of the length of the data series. Therefore, test for lags from 1 to N/4, where N is the length of the data series.
```

 **D.** Fit a multiple linear regression model to the data, using all three meteorological variables (precipitation, maximum temperature, and minimum temperature) to predict April 1 SWE. Report the trend in each meteorological variable. Estimate the overall trend in SWE, and trend due to each meteorological variable alone. How much of the overall trend is due to the combined effects of trends in both maximum and minimum temperature?
 
 ```tip
In part **D** we want to quantify how much a change in each variable accounts for a change in SWE. We start with making a multiple linear regression model, such as one which looks like:

SWE = B0 + B1*(precip) + B2*(t_max) + B3*(t_min)

We then have values for all regression parameters (each B value). Take the derivative of both sides with respect to time. Our regression parameter values are coefficients in this new equation.

dSWE/dt = B1*d(precip)/dt + B2*d(t_max)/dt + B3*d(t_min)/dt

Then to find how much the trend in SWE is accounted for by the trend in precipitation we compute B1*d(precip)/dt, where d(precip)/dt in the slope of the trend in precipitation.
```


### Problem 2: Project Update (CEWA 565)

Provide an update on your term project. By now you should have acquired all of the data you need for your term project.

 **A.** Create 2-3 plots that illustrate your data. These can be time-series plots, histograms, CDFs, whatever is relevant to your data and your problem.
    
 **B.** Discuss the quality of your data. Do you need to take into account any erroneous values or uncertain numbers before you start your statistics?
    
 **C.** Write down at least two very specific questions that you will answer with your data. For each question, write down which statistical tools you will use to help answer it.
    
 **D.** Based on what you have so far, do you think that your project scope is about right for a 10 page paper, or do you feel that you need to either simplify things to make it shorter or add complexity to make it longer? If you feel adjustments are needed, how to you plan to address this issue?
    
 **E.** What do you anticipate being the most difficult parts of your term project? Do you have questions you would like help with or advice on? Write them here.