# Homework 3

## Problem 1: More Hypothesis Testing

Continuing with material from Lab 2-2 and comparing with Homework 2: 

A. **Type II Error**: What is the type II error and power for your test on the mean in the first part of B in Homework 2? 
* To answer this, assume that the true mean has in fact increased by 25%, and pooled standard deviation has increased by a factor of 1.3. In other words, assume that the “true” mean of the later period is 1.25 times the 1929-1976 mean, and that the “true” pooled standard deviation is 1.3 times sigma prime (our test estimate of pooled estimator for the two observed data sets). 
* Draw or plot a graphic to represent this true distribution, and draw where your test statistic falls on this graph. Color the area of the graph that represents Type II error. 
* Then answer the question - what is the type II error and power for your test in part B?

B. **Wilcoxan Rank Sum Test**: 
* Test the significance of the change in the mean between the two sample periods using the two-sample Wilcoxan Rank Sum test. 
* How different is your conclusion from the one in Homework 2. (i.e. compare P for the two tests).

C. **Chi Squared test for a change in the standard deviation**: Lastly test for statistical significance of a change in the standard deviation. 
* Even though it is not strictly true, assume that the sample data are derived from a normally distributed population. (While not required for this homework, we can follow up on the importance of this assumption by using Monte Carlo Tests as shown in Lab 2-3.)
* Use a single sample test (with rejection region based on the Chi Squared distribution), and assume that the sample standard deviation that you calculated from the 1929-1976 data is close to the true population standard deviation that you are testing for a change from.

## Problem 2: Non-Parametric Tests

Download and work through Lab 3-1 on Non-Parametric Tests. One of the challenges in python and statistics is knowing (a) that you picked the right function for your problem and (b) that you understand what the program is actually doing. Read the documentation and source code for the [scipy.stats.ranksums](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ranksums.html) and [scipy.stats.mannwhitneyu](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mannwhitneyu.html) functions.

Then answer the following questions:

**A.** What assumptions about our data and/or the hypothesis test are each of these two functions (ranksums and mannwhitneyu) making? 

**B.** Are there any additional inputs/options we need to specify for either or both functions to make sure that they duplicate our results from the non-parametric tests notebook?

**C.** Examine your answer to Problem 1, part A, using the [observations of peak flow data for the Sauk River](/data/Sauk_peak_WY1929_2021.xlsx) to try and detect a change in streamflow around 1977. Perform the rank-sum test from Problem 1 part A again using the fuction(s) and/or options you identified here. Discuss any differences in the test results that arise from slight differences in these two functions and the options you can choose.


---

**If you've completed the above problems, you can get started on [Problem 1 of Homework 4](/modules/module4/homework4.html#problem-1).**
 
