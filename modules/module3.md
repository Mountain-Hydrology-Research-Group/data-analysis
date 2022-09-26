# 3) Non-Parametric Tests and Analysis of Variance

```note
## Lab 3: Analysis of Variance

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 3-1: ANOVA](lab3/lab3-1.ipynb)
  * data: [ANOVA_fertilizer_treatment.txt](data/ANOVA_fertilizer_treatment.txt)


```

## Homework 3: 

### Problem 1

Continuing with material from Lab 2-2 and comparing with Homework 2, 
A. **Wilcoxan Rank Sum Test**: 
* Test the significance of the change in the mean between the two sample periods using the two-sample Wilcoxan Rank Sum test. 
* How different is your conclusion from the one in Homework 2. (i.e. compare P for the two tests).

B. **Chi Squared test for a change in the standard deviation**: Lastly test for statistical significance of a change in the standard deviation. 
* Even though it is not strictly true, assume that the sample data are derived from a normally distributed population. (While not required for this homework, we can follow up on the importance of this assumption by using Monte Carlo Tests as shown in Lab 2-3.)
* Use a single sample test (with rejection region based on the Chi Squared distribution), and assume that the sample standard deviation that you calculated from the 1929-1976 data is close to the true population standard deviation that you are testing for a change from.

### Problem 2

Download and work through the [non-parametric tests](lab3/non-parametric-tests.ipynb) notebook. Read the documentation and source code for the [scipy.stats.ranksums](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ranksums.html) and [scipy.stats.mannwhitneyu](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.mannwhitneyu.html) functions.

Then answer the following questions:

**A.** What assumptions about our data and/or the hypothesis test are each of these two functions (ranksums and mannwhitneyu) making? 

**B.** Are there any additional inputs/options we need to specify for either or both functions to make sure that they duplicate our results from the non-parametric tests notebook?

**C.** Examine your answer to Problem 1, part A, using the [observations of peak flow data for the Sauk River](data/Sauk_peak_WY1929_2021.xlsx) to try and detect a change in streamflow around 1977. Perform the rank-sum test from Problem 1 part A again using the fuction(s) and/or options you identified here. Discuss any differences in the test results that arise from slight differences in these two functions and the options you can choose.


### If you are able, work ahead, the below will be turned in with Homework 4:

Download the [HJ Andrews Peak Flow data](data/HJAndrews_peakflow_WS1_WS2_WS3.xlsx).

For this problem, consider only differences between watershed 1 (WS1) and watershed 2 (WS2). These two watersheds are adjacent to each other in the [HJ Andrews Experimental Forest](https://andrewsforest.oregonstate.edu/). We want to test if there was a change in streamflow due to the forest within WS1 being completely clearcut (starting late 1962 and completed in 1966). Because the two watersheds are adjacent, we can expect that they experience the same storms leading to peak runoff (so we won't be considering any differences due to different precipitation amounts or timing). 

Here we want to test whether the difference in peak flows between WS1 and WS2 is statistically different for four different time periods:

| Time Period | Years | `Index12` "treatment" label | Notes |
| ----------- | --------------- | --------------- | --------------- |
| control period | 1953-1962 | 1 | before any clearcutting in WS1 |
| active clearcutting | 1963-1966 | 2 | during clearcutting of WS1 |
| 0-15 years after clearcutting | 1967-1981 | 3 | WS1 forest starts to recover |
| >15 years after clearcutting | 1982-2015 | 4 | WS1 forest recovering further |

We want to know whether the four periods are statistically different from each other, and if so, which one or ones are statistically different from which other ones.

 **A.** First, plot the timeseries of the streamflow measurements as a function of water year for both watershed 1 and watershed 2 on the same graph. Use vertical dashed lines ([axvline in matplotlib](https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.axvline.html)) to indicate the different periods (put a vertical dashed line in 1963, in 1967, and in 1982).
 
 **B.** It has been suggested that paired data such as this can be made to be closer to normally distributed by taking the log of each value before subtracting. Create two datasets: `Q12 = streamflow1 - streamflow2` and `Qlog12 = log(streamflow1)- log(streamflow2)` and make graphs to demonstrate which is closer to normally distributed. Given that we want to use an ANOVA analysis, explain why is it important to do a transformation to get the data closer to normally distributed?
 
 **C.** State the null and the alternative hypothesis for the question of whether the four periods are statistically different from each other. State the type I error (alpha value) that you are willing to accept.
 
 **D.** Perform an ANOVA test and discuss the results, related both to your hypothesis test listed above and to the more detailed question of which groups are statistically different from which other groups. Include graphs and/or tables that illustrate your results, and be sure to discuss what they mean. When using these ANOVA and other statistics functions, be sure that you understand what the code is doing (especially the defaults that different functions use) and outputting.
 
