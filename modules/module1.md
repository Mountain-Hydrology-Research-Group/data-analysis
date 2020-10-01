# 1) Python, Statistics Review


```note
## Lab 1: Plotting Random Numbers in Python

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](../resources/b-learning-jupyter.html#jupyterhub).


* [Lab 1-1: Plotting Data in Python](lab1/lab1-1.ipynb)
  * Data: [Skykomish peak flows](data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx)
* [Lab 1-2: Generating Random Numbers in Python](lab1/lab1-2.ipynb)
* [Numpy Tutorial](lab1/numpy-tutorial.ipynb)
* [Some more python tips](lab1/some-python-tips.ipynb)

```


## Homework 1

In this homework assignment we will work start with programming and data visualization to better qualitatively understand the types of datasets that we'll be using the rest of the quarter. **Be sure to save your work for later reference, as you will see these datasets again!**


### Exploring Non-Stationary Flood Statistics


Download the files containing observed instantaneous peak flow data for the [Sauk River](data/Sauk_peak_WY1929_2017.xlsx) and [Skykomish River](data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx) in western Wshington. Note that annual peak flows are reported by water year (Oct 1 of the previous calendar year to September 30), so some calendar years appear to have two values. Water years are shown in an additional column in the excel files. **For the purposes of this assignment, we will only consider peak flows by water year, and the years requested below refer to water years.** (For example, the first flood reported in the Skykomish occurred on Oct 10, 1928 – this is the flood of water year 1929.)

 A. Plot the data from the Sauk River and Skykomish River as a time series from 1929-2009. Use different color lines or symbols to distinguish the two rivers. Be sure to label your axes appropriately and use `plt.legend()` to create a legend. **Describe qualitatively any changes you see in these records through time. Is there a common theme between the two sites?**

 B. **For the Sauk River only**, create and examine the following plots for three time periods: the entire timeseries, all data before 1975, all data from 1975 and later. 
 
 (Make sure that the following plots are well-labeled, readable, and convey meaningful information)
 
  1. **Histograms** for the Sauk River for the entire period and the two sub-periods (3 histograms total)
  2. **Quantile plots** using the Cunnane plotting position (see section 2.1.3 in [Helsel et al., 2020](https://pubs.usgs.gov/tm/04/a03/tm4a3.pdf)) for the Sauk River for the entire period and the two sub-periods. Plot all three lines on the same figure, with different line types/colors and a legend.
  3. **Probability Density Functions** (PDFs) for the Sauk River for the entire period and the two sub-periods. The 3 plots should be plotted on one graph, with different line types and a legend.
  4. **Estimate the sample mean and standard deviation** for each of the two sub-periods (before and after 1975). Assuming a Gaussian (normal) distribution, add theoretical quantile curves to the quantile plots you made earlier. (Theoretical meaning that you're plotting Gaussian Cumulative Density Functions (CDFs) that have the same mean and standard deviation that you calculate). (The plot should now have 6 lines on it – please choose colors and line types to help distinguis them, and label carefully.)
  5. **Box and whisker plots** for each of for the entire period and the two sub-periods, with appropriate labels.
  
 C. Based on all the plots you have now created, write few sentences in a markdown cell discussing whether or not you think a change has occurred in the peak flows around 1975. Be sure to reference your plots (Fig. 1, Fig. 2, etc.) when you discuss them.

---

## In-class activity

We'll do this activity in class, either as a whole or in groups. (This is not part of your homework assignment)

### Fun with fake data!

One of the most reliable tests of any statistical method or technique is to try it out on data where you know the answer to see if the methodology gives you the result you expect. The best way to get data that truly understand is to make it up yourself.

 A. Make up 1000 numbers with a normal distribution, 1000 numbers with a log-normal distribution, and 1000 numbers with a uniform distribution. For each, make the mean be 60 and standard deviation be 40. (You’ll need to think about what the interval should be for the uniform distribution.)

 B. Create descriptive plots (histogram, box and whiskers, quantile plots, PDFs) using all of your samples and compare results from the three distributions. Discuss how you can tell the distributions apart.

 C. Repeat with just 10 numbers from each set, and again with 25 and 100. For each of these, can you tell the distributions apart? What is the sample mean and standard deviation for each?

 D. Discuss the difference between a sample population and the true population.

