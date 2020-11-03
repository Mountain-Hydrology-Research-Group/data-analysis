# 5) Regression, Data Visualization

```note
## Lab 5: Multiple Linear Regression & Regression with Transformed Variables

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Interactive Plots](lab5/interactive-plots.ipynb)
* [Warming Stripes Figure](lab5/warming-stripes.ipynb)
* [Lab 5-1: Multiple Linear Regression](#)
* [Lab 5-2: Regression with Transformed Variables](#)

```

## Homework 5

### Problem 1: Correlation, Autocorrelation, Multiple Linear Regression

Continue using the cascades_swe dataset for this problem. Begin by making scatterplots of each of these variables vs. all the other variables. One nice way to do this is as illustrated in Helsel and Hirsch Figure 2.39 on page 61 – this is not required, you can plot in whatever way works best for you.

 **A.** Calculate the correlation (R) between April 1 SWE and the three meteorological variables (precipitation, max. temperature and min. temperature), and also between all unique combinations of the meteorological variables.
 
 **B.** Calculate the autocorrelation in precipitation, maximum temperature and minimum temperature. Can we consider each of these values to be an independent sample? Or do some of them depend on the prior year’s sample?

```tip
In part **B**, we can test for autocorrelation at different lags, but not for any lag longer than a quarter of the length of the data series. Therefore, test for lags from 1 to N/4, where N is the length of the data series. Determine at which of these lags the autocorrelation is different than 0 with 95% confidence.
```

 **C.** Fit a multiple linear regression model to the data, using all three meteorological variables to predict April 1 SWE. Also calculate the trend in each meteorological variable. Estimate the overall trend in SWE, and trend due to each meteorological variable alone. How much of the overall trend is due to the combined effects of trends in both tmax and tmin?

 **D.** Finally carry out a Mann-Kendall test on the 1950-2003 April 1 SWE data. Is the trend significant according to this test? Compare your answer with your regression analysis for the same data in Problem 2B. **Note:** For this problem you do not need to worry about the tie statistic.


### Problem 2: Calculating a rating curve and associated uncertainty

Download Tuolumne_120_stage_Q_2002_2018_forclass.csv (also available in the data folder or the Homework 4 folder on the class Canvas website). Make a scatter plot of stage (in cm) vs. discharge (in cms). You may want to look at Venetis_1970.pdf (also available in the Readings/Rating_Curve_Analysis folder on Canvas). 

Plot the data, assume that h0 =70 cm, the stage height at which flow stops. This is a guess, but for now, we’ll assume this is truth. Use linear regression with transformed variables to fit an equation of the form Q=a(h-h0)b to the data, to determine a and b, where Q is discharge in cms, and h is stage in cm. Determine 95% confidence intervals for b (note this corresponds to B1 in class lecture) and for log(Q). Transform the mean, upper, and lower confidence intervals for log(Q) back to Q, and plot the rating curve with confidence intervals and the original data.

Now, assume that we don’t know at what level flow stops. Repeat the above for h0 = 60, 65, 70, 75, and 80 cm. Recalculate a, b, log(Q), and Q for each of these. Don’t worry about 95% uncertainty in this example. Make a plot showing stage (h) vs. Q for each of these 5 cases. Is the range between these 5 lines larger or smaller than the range between the 95% confidence lines that you generated before? Note that we did not explicitly account for uncertainty in h0 in generating those 95% confidence lines. Based on what you have plotted here, is that an okay thing to do or not?

The data provided in the file also have uncertainty associated with them. Describe in a couple sentences how you would account for this uncertainty. (Note that you do not need to do more calculations. Just write a couple sentences about things you might do.)


### Problem 3: Project Update (Graduate Students)

Provide an update on your term project. By now you should have acquired all of the data you need for your term project.

 **A.** Create 2-3 plots that illustrate your data. These can be time-series plots, histograms, CDFs, whatever is relevant to your data and your problem.
    
 **B.** Discuss the quality of your data. Do you need to take into account any erroneous values or uncertain numbers before you start your statistics?
    
 **C.** Write down at least two (more are also okay) very specific questions that you will answer with your data. For each question, write down which statistical tools you will use.
    
 **D.** Based on what you have so far, do you think that your project scope is about right for a 10-page paper, or do you feel that you need to either simplify things to make it shorter or add complexity to make it longer? If you feel adjustments are needed, how to you plan to address this issue?
    
 **E.** At this point, what do you anticipate being the most difficult parts of your term project? Do you have questions you would like help with or advice on? Write them here.