# Week 1


```note
## Lab 1: Plotting Random Numbers in Python

Download the data file and the lab files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 1-0: Python tips](lab1/lab1-0.ipynb)
* [Lab 1-1: Plotting Data in Python](lab1/lab1-1.ipynb)
  * Data: [Skykomish peak flows](data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx)
* [Lab 1-2: Generating Random Numbers in Python](lab1/lab1-2.ipynb)

```


## Homework 1

In this homework assignment we will work with programming and data visualization to better qualitatively understand the datasets that we will be using in the upcoming homework assignments for the rest of the quarter. Be sure to save your work, as you will see these datasets again!


### Problem 1: Exploring Non-Stationary Flood Statistics


Download the files containing observed instantaneous peak flow data for the Sauk River and Skykomish Rivers in western WA. Note that annual peak flows are reported by water years (which cover Oct 1 of the previous year to September 30), so some years appear to have two values. (For clarification, the water years are shown in an additional column in the excel files.) For the purposes of this assignment, we will only consider peak flows by water year, and the years requested below refer to water years. (For example, the first flood reported in the Skykomish occurred on Oct 10, 1928 – this is the flood of water year 1929.)

 A. Plot the data from the two streamflow sites as a time series from 1929-2009, with an open circle representing each peak flow value. Be sure to label your axes appropriately and label which graph is associated with which river. Describe qualitatively any changes you see in these records through time. Is there a common theme between the two sites?

 B. For the Sauk River only, graphically examine the entire timeseries and the peak flows occurring before and after 1975 (1929-1974, and 1975-2017). Prepare the following plots, taking care to make sure that they are well-labeled, readable, and convey meaningful information.
 
  1. Histograms for the Sauk River for the entire period and each of the sub- periods (3 total).
  2. Quantile plots using the Cunnane plotting position (see section 2.1.3 in H&H) for the Sauk River for the entire period, and for each sub-period. The 3 plots should be plotted on one graph, with different line types and a legend.
  3. PDFs for the Sauk River for the entire period, and for each sub-period. The 3 plots should be plotted on one graph, with different line types and a legend.
  4. For each of the sub-groupings in 2, estimate the sample mean and standard deviation. Assuming a Gaussian distribution, add theoretical curves to the plots in 2 for Gaussian CDFs that have the same means and standard deviations as calculated for the actual data. (The graph should now have 6 lines – label carefully.)
  5. Box and whisker plots for each of the periods above (total, pre-1975 and 1975-present), with appropriate labels.
 F. Based on the plots you have created, discuss whether or not you think a change has occurred in the peak flows around 1975. Be sure to reference your plots (Fig. 1, Fig. 2, etc.) when you discuss them.



### Problem 2: Fun with fake data!

One of the most reliable tests of any statistical method or technique is to try it out on data where you know the answer to see if the methodology gives you the result you expect. The best way to get data that truly understand is to make it up yourself.

 A. Make up 1000 numbers with a normal distribution, 1000 numbers with a log-normal distribution, and 1000 numbers with a uniform distribution. For each, make the mean be 60 and standard deviation be 40. (You’ll need to think about what the interval should be for the uniform distribution.)

 B. Create descriptive plots (histogram, box and whiskers, quantile plots, PDFs) using all of your samples and compare results from the three distributions. Discuss how you can tell the distributions apart.

 C. Repeat with just 10 numbers from each set, and again with 25 and 100. For each of these, can you tell the distributions apart? What is the sample mean and standard deviation for each?

 D. Discuss the difference between a sample population and the true population.

