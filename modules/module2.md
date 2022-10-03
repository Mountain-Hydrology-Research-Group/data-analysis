# 2) Hypothesis Testing

- [Confidence Intervals](lab2/confidence-intervals.ipynb) with our [snow depth guesses](data/snow_depth_guesses.csv)

```note
## Lab 2: Hypothesis Testing

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* Data: [Skykomish peak flows](data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx) 
* [Lab 2-1: Hypothesis Testing](lab2/lab2-1.ipynb)  ([Solution to Lab 2-1 activity](lab2/lab2-1_solution.ipynb))
* [Lab 2-2: More Hypothesis Testing](lab2/lab2-2.ipynb)
* BONUS, not required for homework: [Lab 2-3: Monte Carlo Tests](lab2/lab2-3.ipynb)

```



## Homework 2

### Problem 1

Using the [observations of peak flow data for the Sauk River](data/Sauk_peak_WY1929_2021.xlsx), we are going to investigate whether a change in flood statistics occurred around 1977.

A. **Descriptive Plots**: Decide which of your plots from Homework 1 are relevant to the question of whether a change in flood statistics occurred in the Sauk River around 1977. 
* Include these plots from Homework 1 here.
* Discuss what you can see visually in the graphs that would lead you to believe that a change has or has not occurred.

B. **Two-sample test for a change in the mean**: Test for statistical significance of the observed change in the mean annual peak flow around 1977. 
* Use a two sample test, and alpha = 0.05 (95% confidence) and the z-distribution to define the rejection region. 
* Discuss why using the z-distribution is appropriate here. 
* Use the two-sample test to compare the data from 1977-2021 to the data from 1929-1976, accounting for the different sample sizes and sample standard deviations appropriately (remember to use the "pooled standard deviation"). 
* For your null hypothesis, postulate that the difference between the two means = 0, and state the alternative hypothesis that the difference has changed (although you don’t know the direction of this change) and state the test statistic you'll be using. 
* Can you reject the null hypothesis? 
* Calculate P after your test. 
* How does your estimate of P change if your null hypothesis is that the difference in the mean between the two data sets is equal to 25% of the pre-1977 sample mean? (In other words, test with a new null hypothesis: the mean of the second period is 1.25 times the mean of the first period.)


### Problem 2: Course Project Selection (CEWA 565 only)

Write a brief paragraph (3-9 sentences) describing your term project. Include the name of your partner (or specify you will be doing the project alone), the data you will analyze, and which question(s) you will answer. Which statistical tools will you use? If you have a hypothesis to test, write it down. **If you have questions about the project, now is the time to talk to the instructor.**
