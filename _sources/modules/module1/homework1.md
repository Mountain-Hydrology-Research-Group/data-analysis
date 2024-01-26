# Homework 1

In this homework assignment we will start with programming and data visualization to better qualitatively understand the types of datasets that we'll be using the rest of the quarter.  Please download the notebooks at the top of this page and use them as reference for your coding.  **Be sure to save your work for later reference, as you will see these datasets again!**


## Problem 1: Exploring Non-Stationary Flood Statistics


Download the files containing observed instantaneous peak flow data for the {Download}`Sauk River</modules/data/Sauk_peak_WY1929_2021.xlsx>` and {Download}`Skykomish River</modules/data/Skykomish_peak_flow_12134500_skykomish_river_near_gold_bar.xlsx>` in western Washington. If you are interested in other rivers, e.g., for your project, these data can be obtained from the [USGS](https://nwis.waterdata.usgs.gov/nwis/peak?search_criteria=search_station_nm&submitted_form=introduction).

Note that annual peak flows are reported by water year (Oct 1 of the previous calendar year to September 30), so some calendar years appear to have two values. Water years are shown in an additional column in the excel files. **For the purposes of this assignment, we will only consider peak flows by water year, and the years requested below refer to water years.** (For example, the first flood reported in the Skykomish occurred on Oct 10, 1928 – this is the flood of water year 1929.)

 A. Plot the data from the Sauk River and Skykomish River as a time series from 1929-2021. Use different color lines or symbols to distinguish the two rivers. Be sure to label your axes appropriately and use `plt.legend()` to create a legend. **Describe qualitatively any changes you see in these records through time. Is there a common theme between the two sites?**

 B. We know that in water year 1977, there was a large [PDO](https://en.wikipedia.org/wiki/Pacific_decadal_oscillation) shift in the North Pacific, and we want to know if floods were statistically different before and after this date. In this homework, we will graphically examine the data. 
 
 **For the Sauk River only**, create and examine the following plots for two time periods: all data before 1977, all data from 1977 and later. 
 
 (Make sure that the following plots are well-labeled, readable, and convey meaningful information)
 
  1. **Histograms** for the Sauk River for the two sub-periods (2 histograms total)
  2. **Quantile plots** using the Cunnane plotting position (see section 2.1.3 in [Helsel et al., 2020](https://pubs.usgs.gov/tm/04/a03/tm4a3.pdf)) for the Sauk River for the two sub-periods. Plot the two lines on the same figure, with different line types/colors and a legend.
  3. **Probability Density Functions** (PDFs) for the Sauk River for the two sub-periods. The 2 plots should be plotted on one graph, with different line types and a legend.
  4. **Estimate the sample mean and standard deviation** for each of the two sub-periods (before and after 1977). Assuming a Gaussian (normal) distribution, add theoretical quantile curves to the quantile plots you made earlier. (Theoretical meaning that you're plotting Gaussian Cumulative Density Functions (CDFs) that have the same mean and standard deviation that you calculate). (The plot should now have 4 lines on it – please choose colors and line types to help distinguis them, and label carefully.)
  5. **Box and whisker plots** for each of the two sub-periods, with appropriate labels.
  
 C. Based on all the plots you have now created, write a few sentences in a markdown cell discussing whether or not you think a change has occurred in the peak flows around 1977. Be sure to reference your plots (Fig. 1, Fig. 2, etc.) when you discuss them.

---
