# Homework 3

Continuing with material from Lab 2 and comparing with Homework 2, using the {Download}`observations of peak flow data for the Sauk River</modules/data/Sauk_peak_WY1929_2025.xlsx>`:

## Problem 1: Type II Error
Here you will determine the type II error and power for your test on the mean in the first part of B in Homework 2. To answer this, assume that the true mean has in fact increased by 25%, and pooled standard deviation has increased by a factor of 1.5. In other words, assume that the “true” mean of the later period is 1.25 times the 1929-1976 mean, and that the “true” pooled standard deviation is 1.5 times sigma prime (our test estimate of pooled estimator for the two observed data sets). 

**A.** What are the type II error and power for the test in HW2?

**B.** Draw or plot a graphic to represent this true distribution, and draw where your test statistic falls on this graph. Color the area of the graph that represents Type II error.

**C.** Repeat the above, but change your Type I error to 20%.  In other words, change from alpha=0.05 to alpha=0.20.  How does this change the Type II error and power?   Create another graph where you color the area that represents the Type II error for the situation with more Type I error.

## Problem 2: Rank-Sum Test
Download and work through Labs 3-1 and 3-2 on Non-Parametric Tests. One of the challenges in python and statistics is knowing (a) that you picked the right function for your problem and (b) that you understand what the program is actually doing. Read the documentation and source code for the [scipy.stats.ranksums](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ranksums.html) and [scipy.stats.mannwhitneyu](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mannwhitneyu.html) functions.  Note that it is helpful for this problem to read Section 5.1 in Ch 5 in Helsel and Hirsch before you read the code.  Then, think about how the two functions are similar and how they differ.

**A.** Answer the following questions:
* What assumptions about our data and/or the hypothesis test are each of these two functions (ranksums and mannwhitneyu) making? 
* Are there any additional inputs/options we need to specify for either or both functions to make sure that they duplicate our results from the non-parametric tests notebook?
* Which of these functions (or both, or neither) are appropriate for the example here?

**B.** Then do the following:
* Test the significance of the change in the mean between the two sample periods using the two-sample Rank-Sum test. 
* How different is your conclusion from the one in Homework 2. (i.e. compare P for the two tests).

## Problem 3: Empirical Test of the Central Limit Theorem: 
Following Lab 1-4, draw 35 random numbers from a uniform distribution with a mean of 100 and standard deviation of 50 (same mean and sd as in the lab). (Note that the solution to the Lab 1-4 activity is available for download on the main Module 1 page.)  Create a histogram for these 35 numbers and plot.  What type of distribution does it look like?  What are the empirical mean and variance of these 35 numbers?

Now create a loop where you repeat this 1000 times.  Each time, draw 35 random numbers from the uniform distribution, calculate the empirical mean and variance of those 35 numbers, and save those values.  So, you should have 1000 mean values and 1000 variances.  Create histograms for the means and the variances.  What type of distribution do each of these look like?  Relate your results here to the discussions in class about the Central Limit Theorem and when it applies.

---
 
## Problem 4: Peer Reviews (CEWA 565 only)

Complete the peer review(s) that you were assigned on Canvas. You are reviewing the abstract (overview) of another group's proposed project. Your review should be thoughtful, but it does not need to be long, nor does it need to focus on minor spelling or grammar mistakes. Write a few sentences describing the most important change that can be made to improve the draft (e.g. "reorganize the paragraphs to better explain X", "add more supporting evidence for the topic statement"). At this point, the most common comment is that an idea needs to be better clarified, or it's uncertain if there's enough data to actually do a statistical test.  Refer to the prior homework assignment to see guidelines for the draft project reports. (the rubric for the final report is available for your reference [here](/overview/b-project.md))
