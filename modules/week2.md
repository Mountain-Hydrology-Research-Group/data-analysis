# Week 2


```note
## Lab 2: Hypothesis Testing

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* Data: [Skykomish peak flows](data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx) 
* [Lab 2-1: Hypothesis Testing 1](lab2/lab2-1.ipynb)
* [Lab 2-2: Hypothesis Testing 2](lab2/lab2-2.ipynb)
* [Lab 2-3: Hypothesis Testing 3](lab2/lab2-3.ipynb)

```



## Homework 2

### Problem 1


A. Decide which of your plots from Homework 1 are relevant to the questions of whether a change in flood statistics occurred in the Sauk around 1977. Include these graphs here and discuss what you can see visually in the graphs that would lead you to believe that a change has or has not occurred.	

B. (Make sure you are using the updated data through 2017.) Postulating a change in flood statistics around 1977, test for statistical significance of the observed change in the mean annual flood. Use a two sample test, and alpha = 0.05 (i.e. 95% confidence) and the z distribution to define the rejection region (why is this appropriate?). Compare the period from 1977-2017 to the data from 1929-1976, accounting for the different sample sizes and sample standard deviations appropriately. For your null hypothesis, postulate that the difference between the two means = 0, and state the alternative hypothesis that the difference has changed (although you don’t know the direction of this change) and the appropriate test statistic. Can you reject the null hypothesis? Calculate P. How would your estimate of P change if your null hypothesis is that the difference in the mean between the two data sets is equal to 15% of the pre-1977 sample mean? (In other words, the null hypothesis is that the mean of the second period is 1.15 times the mean of the first period.)

C. What is the type II error and power for your test on the mean in the first part of B above? To answer this, assume that the true mean has in fact increased by 15%, and pooled standard deviation has increased by a factor of 1.15. In other words, assume that the “true” mean is 1.15 times the 1929-1976 mean, and that the “true” pooled standard deviation is 1.15 times sigma prime (our test estimate of pooled estimator for the two observed data sets). Draw a graphic to represent this true distribution, and draw where your test statistic falls on this graph. Color the area of the graph that represents type II error. Then answer the question (what is the type II error and power for your test in part B).

D. Now test the significance of the change in the mean between the two sample periods using the two-sample Wilcoxan Rank Sum test. How different is your conclusion from the one in part B. (i.e. compare P for the two tests).

E. Lastly test for statistical significance of a change in the standard deviation. Even though it is not strictly true, assume for the moment that the sample data are derived from a normally distributed population. (We will follow up on the importance of this assumption in problem 2.) Use a single sample test (with rejection region based on the Chi Squared distribution). Assume that the sample standard deviation that you calculated from the 1929-1976 data is close to the true population standard deviation that you are testing for a change from.


### Problem 2: Monte Carlo Tests

In this exercise we will estimate the statistical significance of the changes in the mean and standard deviation in Problem 1 using a Monte Carlo approach. Conduct the analysis for the Sauk Data peak flows for water years 1929 to 2017. Start by creating CDFs of annual peak flow for the two periods of analysis in Problem 1, using the Cunnane quantile estimator discussed in class. Note: If you are using VLOOKUP in Excel, you will need to linearly extend your CDF to 0 and 1 so that you can translate all values.

A. Generate 500 samples, each with n = 41 (the length of the 1977-2017 dataset), assuming the CDF from the 1929-1976 data from problem 1. Use the uniform random number generator in Matlab (or Excel if you are struggling with Matlab, although it will take longer in Excel) and the CDF you created above, following the methods discussed in class (see the sample spreadsheet referenced in the notes for specific coding details).  
B. For each of the 500 samples, calculate the sample mean and standard deviation.  
C. Take the 500 sample means and sample standard deviations from part B and fit an unbiased quantile estimator to them to obtain a CDF of the means and standard deviations.  
D. Extract the upper tailed 95% confidence value from this CDF for the mean and standard deviations (i.e. make a table of quantiles close to 0.95 and their associated values)  
E. Using the sample mean and standard deviation from the 1977-2017 data in problem 1, what would you conclude about the statistical significance of these values (alpha = 0.05). That is, based on the quantiles from your Monte Carlo analysis, are the observed values from 1977-2017 statistically significant for alpha = 0.05. Are these conclusions substantially different from those in Problem 1 part B and E? (In other words, compare P in the two tests. You can determine P by the quantile values associated with the CDFs you generated here.)


### Problem 3: Course Project Selection (Graduate Students)

Write a brief paragraph (3-9 sentences) describing your term project. Include the name of your partner (or specify you will be doing the project alone), the data you will analyze, and which question(s) you will answer. Which statistical tools will you use? If you have a hypothesis to test, write it down. If you have questions about the project, now is the time to talk to the instructor.
