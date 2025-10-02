# Homework 3

Continuing with material from Lab 2 and comparing with Homework 2, using the {Download}`observations of peak flow data for the Sauk River</modules/data/Sauk_peak_WY1929_2025.xlsx>`:

## Problem 1: Type II Error
Here you will determine the type II error and power for your test on the mean in the first part of B in Homework 2. To answer this, assume that the true mean has in fact increased by 25%, and pooled standard deviation has increased by a factor of 1.5. In other words, assume that the “true” mean of the later period is 1.25 times the 1929-1976 mean, and that the “true” pooled standard deviation is 1.5 times sigma prime (our test estimate of pooled estimator for the two observed data sets). 

**A.** What are the type II error and power for the test in HW2?

**B.** Draw or plot a graphic to represent this true distribution, and draw where your test statistic falls on this graph. Color the area of the graph that represents Type II error.

## Problem 2: Rank-Sum Test
Download and work through Labs 3-1 and 3-2 on Non-Parametric Tests. One of the challenges in python and statistics is knowing (a) that you picked the right function for your problem and (b) that you understand what the program is actually doing. Read the documentation and source code for the [scipy.stats.ranksums](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ranksums.html) and [scipy.stats.mannwhitneyu](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mannwhitneyu.html) functions.  Note that it is helpful for this problem to read Section 5.1 in Ch 5 in Helsel and Hirsch before you read the code.  Then, think about how the two functions are similar and how they differ.

**A.** Answer the following questions:
* What assumptions about our data and/or the hypothesis test are each of these two functions (ranksums and mannwhitneyu) making? 
* Are there any additional inputs/options we need to specify for either or both functions to make sure that they duplicate our results from the non-parametric tests notebook?
* Which of these functions (or both, or neither) are appropriate for the example here?

**B.** Then do the following:
* Test the significance of the change in the mean between the two sample periods using the two-sample Rank-Sum test. 
* How different is your conclusion from the one in Homework 2. (i.e. compare P for the two tests).

## Problem 3: Chi Squared test for a change in the standard deviation: 
Lastly, test for statistical significance of a change in the standard deviation. Even though it is not strictly true, assume that the sample data are derived from a normally distributed population. (While not required for this homework, we can follow up on the importance of this assumption by using Monte Carlo Tests as shown in Lab 2-3.)

Use a single sample test (with rejection region based on the Chi Squared distribution), and assume that the sample standard deviation that you calculated from the 1929-1976 data is close to the true population standard deviation that you are testing for a change from.

---
 
## Problem 4: Peer Reviews (CEWA 565 only)

Complete the peer review(s) that you were assigned on Canvas. You are reviewing the abstract (overview) of another group's proposed project. Your review should be thoughtful, but it does not need to be long, nor does it need to focus on minor spelling or grammar mistakes. Write a few sentences describing the most important change that can be made to improve the draft (e.g. "reorganize the paragraphs to better explain X", "add more supporting evidence for the topic statement"). At this point, the most common comment is that an idea needs to be better clarified, or it's uncertain if there's enough data to actually do a statistical test.  Refer to the prior homework assignment to see guidelines for the draft project reports. (the rubric for the final report is available for your reference [here](/overview/b-project.md))
