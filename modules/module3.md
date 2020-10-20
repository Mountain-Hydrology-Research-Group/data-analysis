# 3) Correlation, Regression


```note
## Lab 3: ANOVA and Regression

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 3-1: ANOVA](lab3/lab3-1.ipynb)
  * data: [ANOVA_fertilizer_treatment.txt](data/ANOVA_fertilizer_treatment.txt)
* [Lab 3-2: Regression](#)
  * data: [pillows_example.csv](data/pillows_example.csv)
* [Lab 3-3: Quantile Regression Modeling](#)
* [Lab 3-4: Confidence Intervals](#)


```



## Homework 3: 

### Problem 1

Download the [HJ Andrews Peak Flow data](data/HJAndrews_peakflow_WS1_WS2_WS3.xlsx).

For this problem, consider only differences between watershed 1 (WS1) and watershed 2 (WS2). These two watersheds are adjacent to each other in the [HJ Andrews Experimental Forest](https://andrewsforest.oregonstate.edu/). We want to test if there was a change in streamflow due to the forest within WS1 being completely clearcut (starting late 1962 and completed in 1966). Because the two watersheds are adjacent, we can expect that they experience the same storms leading to peak runoff (so we won't be considering any differences due to different precipitation amounts or timing). 

Here we want to test whether the difference in peak flows between WS1 and WS2 is statistically different for four different time periods:

| Time Period | Years | `Index12` "treatment" label | Notes |
| ----------- | --------------- | --------------- | --------------- |
| control | 1953-1962 | 1 | before any clearcutting in WS2 |
| active clearcutting | 1963-1966 | 2 | during clearcutting of WS2 |
| 0-15 years after clearcutting | 1967-1981 | 3 | when we the forest starts to recover |
| >15 years after clearcutting | 1982-2015 | 4 | when the forest is recovering further |

We want to know whether the four periods are statistically different from each other, and if so, which one or ones are statistically different from which other ones.

 **A.** First, plot the timeseries of the streamflow measurements as a function of water year for both watershed 1 and watershed 2 on the same graph. Use vertical dashed lines ([axvline in matplotlib](https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.axvline.html)) to indicate the different periods (put a vertical dashed line in 1963, in 1967, and in 1982).
 
 **B.** It has been suggested that paired data such as this can be made to be closer to normally distributed by taking the log of each value before subtracting. Create two datasets: `Q12 = streamflow1 - streamflow2` and `Qlog12 = log(streamflow1)- log(streamflow2)` and make graphs to demonstrate which is closer to normally distributed. Given that we want to use an ANOVA analysis, explain why is it important to do a transformation to get the data closer to normally distributed?
 
 **C.** State the null and the alternative hypothesis for the question of whether the four periods are statistically different from each other. State the type I error (alpha value) that you are willing to accept.
 
 **D.** Perform an ANOVA test and discuss the results, related both to your hypothesis test listed above and to the more detailed question of which groups are statistically different from which other groups. Include graphs and/or tables that illustrate your results, and be sure to discuss what they mean. When using these ANOVA and other statistics functions, be sure that you understand what the code is doing (especially the defaults that different functions use) and outputting.
 
### Problem 2
 
Download the Dalles peak flow data.
 
USGS gaged streamflow records for the Columbia River at The Dalles, OR began in 1878 and continues to the present day (one of the longest continuous records in the U.S.). Peak flow records (based on peak stage values recorded by railroad workers), however, extend back even farther, to 1858. Using coincident peak flow records from 1879-1932 (a period with no major storage dams on the Columbia):

 **A.** First, isolate the period of relevant overlap (1879-1932) and plot the timeseries. Create a regression model for annual flow using spring peak flow as an explanatory variable.
 
 **B.** How much of the variance is explained by the resulting model?
 
 **C.** Estimate the 95% confidence bounds for the annual flow estimates from 1858- 1877, and plot them with the central tendency (the prediction from the regression model).
 
 **D.** Now create a non-parametric, quantile-based regression model using the same data.
 
 **E.** Plot the predictions and residuals for the two different prediction models for the training period (1879-1932) and plot the model predictions for the pre-1878 data for the two different models. Is there a substantial difference between the two model formulations?
 
