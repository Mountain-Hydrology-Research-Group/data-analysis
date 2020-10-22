# 2) Hypothesis Testing

- [Confidence Intervals](lab2/confidence-intervals.ipynb) with our [snow depth guesses](data/snow_depth_guesses.csv)
- [Non-parametric tests](lab2/non-parametric-tests.ipynb) ([Solution to non-parametric tests activity](lab2/non-parametric-tests_solution.ipynb))

```note
## Lab 2: Hypothesis Testing

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* Data: [Skykomish peak flows](data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx) 
* [Lab 2-1: Hypothesis Testing](lab2/lab2-1.ipynb)  ([Solution to Lab 2-1 activity](lab2/lab2-1_solution.ipynb))
* [Lab 2-2: More Hypothesis Testing](lab2/lab2-2.ipynb)
* [Lab 2-3: Monte Carlo Tests](lab2/lab2-3.ipynb)

```



## Homework 2

### Problem 1

Using the [observations of peak flow data for the Sauk River](data/Sauk_peak_WY1929_2017.xlsx), we are going to investigate whether a change in flood statistics occurred around 1977.

A. **Descriptive Plots**: Decide which of your plots from Homework 1 are relevant to the question of whether a change in flood statistics occurred in the Sauk River around 1977. 
* Include these plots from Homework 1 here
* Discuss what you can see visually in the graphs that would lead you to believe that a change has or has not occurred

B. **Two-sample test for a change in the mean**: Test for statistical significance of the observed change in the mean annual peak flow around 1977. 
* Use a two sample test, and alpha = 0.05 (95% confidence) and the z-distribution to define the rejection region. 
* Discuss why using the z-distribution is appropriate here. 
* Use the two-sample test to compare the data from 1977-2017 to the data from 1929-1976, accounting for the different sample sizes and sample standard deviations appropriately (remember to use the "pooled standard deviation"). 
* For your null hypothesis, postulate that the difference between the two means = 0, and state the alternative hypothesis that the difference has changed (although you don’t know the direction of this change) and state the test statistic you'll be using. 
* Can you reject the null hypothesis? 
* Calculate P after your test. 
* How does your estimate of P change if your null hypothesis is that the difference in the mean between the two data sets is equal to 15% of the pre-1977 sample mean? (In other words, test with a new null hypothesis: the mean of the second period is 1.15 times the mean of the first period.)

C. **Type II Error**: What is the type II error and power for your test on the mean in the first part of B above? 
* To answer this, assume that the true mean has in fact increased by 15%, and pooled standard deviation has increased by a factor of 1.15. In other words, assume that the “true” mean is 1.15 times the 1929-1976 mean, and that the “true” pooled standard deviation is 1.15 times sigma prime (our test estimate of pooled estimator for the two observed data sets). 
* Draw or plot a graphic to represent this true distribution, and draw where your test statistic falls on this graph. Color the area of the graph that represents Type II error. 
* Then answer the question - what is the type II error and power for your test in part B?

D. **Wilcoxan Rank Sum Test**: 
* Now test the significance of the change in the mean between the two sample periods using the two-sample Wilcoxan Rank Sum test. 
* How different is your conclusion from the one in part B. (i.e. compare P for the two tests).

E. **Chi Squared test for a change in the standard deviation**: Lastly test for statistical significance of a change in the standard deviation. 
* Even though it is not strictly true, assume that the sample data are derived from a normally distributed population. (We can follow up on the importance of this assumption in problem the Monte Carlo Tests activity below)
* Use a single sample test (with rejection region based on the Chi Squared distribution), and assume that the sample standard deviation that you calculated from the 1929-1976 data is close to the true population standard deviation that you are testing for a change from.

### Problem 2: Course Project Selection (CEWA 565)

Write a brief paragraph (3-9 sentences) describing your term project. Include the name of your partner (or specify you will be doing the project alone), the data you will analyze, and which question(s) you will answer. Which statistical tools will you use? If you have a hypothesis to test, write it down. **If you have questions about the project, now is the time to talk to the instructor.**
