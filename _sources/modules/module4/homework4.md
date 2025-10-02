# Homework 4

## Problem 1: ANOVA

This problem is based on material in Lab 3-3.

Download the {Download}`HJ Andrews Peak Flow data</modules/data/HJAndrews_peakflow_WS1_WS2_WS3.xlsx>`.

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
 
 **B.** It has been suggested that paired data such as this can be made to be closer to normally distributed by taking the log of each value before subtracting. Create two datasets: `Q12 = streamflow1 - streamflow2` and `Qlog12 = log(streamflow1)- log(streamflow2)` and make graphs to demonstrate which is closer to normally distributed. Given that we want to use an ANOVA analysis, explain why is it important to check if a transformation might get the data closer to normally distributed?
 
 **C.** State the null and the alternative hypothesis for the question of whether the four periods are statistically different from each other. State the type I error (alpha value) that you are willing to accept.
 
 **D.** Perform an ANOVA test and discuss the results, related both to your hypothesis test listed above and to the more detailed question of which groups are statistically different from which other groups. Include graphs and/or tables that illustrate your results, and be sure to discuss what they mean. When using these ANOVA and other statistics functions, be sure that you understand what the code is doing (especially the defaults that different functions use) and outputting.
 

## Problem 2: Linear and Quantile Regression

Download the {Download}`streamflow records for the Columbia River</modules/data/dalles_flow.csv>`.
 
Streamflow records for the Columbia River measured at The Dalles, Oregon, began in water year 1879 and continues to the present day (this is one of the longest continuous records of streamflow in the U.S.). Peak flow records extend back to 1858 (based on peak stage values recorded by railroad workers). 

Using the coincident peak flow records from 1879-1933 (also a period with no major storage dams on the Columbia), create models to predict annual flow for years 1858-1878:

 **A.** Isolate the period of relevant overlap for annual and peak flow records (1879-1933) and plot a timeseries of these measurements. Then create a least-squares linear regression model to predict annual flow using peak flow as an explanatory variable.
 
 **B.** How much of the true variance of annual flow is explained by the resulting model?
 
 **C.** Now create a non-parametric, quantile-based regression model using the same data.
 
 **D.** Plot the predictions and residuals for the two different prediction models for the training period (1879-1933), and plot the model predictions for the 1858-1878 data for the two different models. Is there a substantial difference between the two model formulations? Discuss any differences that you observe.
 

## Problem 3: Project Update (CEWA 565)

Upload this part of the assignment as a separate PDF or Word document to "Homework 4 Project Update" on Canvas.

Submit an updated draft abstract along with a draft introduction section. The introduction section should provide more details about the project and any relevant background information, the science questions and hypotheses you will be addressing, and the data you will be using. Include at least two very specific questions that you will answer with your data. For each question, write down which statistical tools you will use to help answer it.  Include one or two plots that illustrate your data. These can be time-series plots, histograms, CDFs, or whatever is relevant to your data and your problem.

```{note}
Based on what you have so far, do you think that your project scope is about right for a 10 page paper, or do you feel that you need to either simplify things to make it shorter or add complexity to make it longer? 

If you feel adjustments are needed, how to you plan to address this issue? 

What do you anticipate being the most difficult parts of your term project? 

Do you have questions you would like help with or advice on? 

If so, include them in your homework submission or set up a meeting to discuss them with the instructor.
```

(the rubric for the final report is available for your reference [here](/overview/b-project.md))
