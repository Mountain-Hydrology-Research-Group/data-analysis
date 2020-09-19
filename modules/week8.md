# Week 8: SVD, Timeseries Analysis


```note
## Lab 8:

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 8-1: SVD with Monthly Precip.](lab8/lab8-1.iynb)
  * data: [PRISM_4km_1982-2012.mat](data/PRISM_4km_1982-2012.mat)
* [Lab 8-1: Timeseries Lab](lab8/lab8-2.iynb)	

```


## Homework 8

### Problem 1: Air Temperature Observations in Complex Terrain

 Download the file “iButtons_2008-2010.mat” (available below, or from the Files/Week 08 folder on Canvas). It contains hourly air temperature [°C] observations from 21 distributed sensors (iButtons) located around the watershed of the North Fork of the American River in the Sierra Nevada of California, over a period from September 2007 to July 2010. It also contains information about the sites’ names, numbers, coordinates and elevations. See Fig. 1 for a map of the sites. 

Figure 1: iButton locations and topographic shading. The sites are located around the American River canyon on the west slope of the Sierra Nevada Mountains in California. Lake Tahoe is the large flat area in the southeast portion of the map.


 **A.** Plot the temperature observations (AIR _TEMPERATURE) at all sites on one plot over time; use the title, xlabel, and ylabel commands to label your plot and its axes. Use xlim to zoom in and examine the data at finer scales. Qualitatively describe the dataset, including its minimum and maximum values, its major variability in time, and how correlated the stations appear to be with one another.
 
 **B.** Use the command: [U,S,V] = svd(AIR_TEMPERATURE_ZEROMEAN,False) to calculate the PCs, variances, and EOFs, respectively, of a version of the dataset where the mean temperature at each station has been subtracted out. Describe how the variance is distributed among the patterns; how much is described by the leading pattern? By the second pattern?
 
 **C.** Plot the leading pattern’s spatial weights (EOF) against latitude and longitude. Describe the first pattern’s spatial weights’ sign and variability.
 
 **D.** Plot the leading pattern’s temporal weights (PCs). When are they positive and when are they negative? Consider the PCs’ sign and magnitude, and consider the sign of the EOF in Part C. When does this pattern generate warmer-than-normal temperatures? Colder-thannormal temperatures? Are the anomalies associated with this pattern of the same sign at all sites?
 
 **E.** Repeat C) and D) for the 2nd-leading pattern. Interpret physically what the first two patterns may represent. How much of the dataset is described by the first two modes of variability?

 
### Problem 2: Timeseries Analysis 
 
Download the file “waterlevel.mat” (provided below, or from the Files/Data folder of the course website). It contains hourly measurements of water level (Level, in cm) from an unidentified site for one year. The sampling frequency, sf, is 24, and the timeseries, t, is in days. Plot the data and zoom in to see what’s going on. Use the timeseries analysis techniques we discussed in lab to plot the spectral density of this data. Do this both for the entire timeseries and for four equal-sized chunks of the data. From these plots, identify whether the noise associated is with this data series is red noise or white noise, and identify at what frequencies the timeseries varies. Based on what you find, where do you think this water level measurement was taken? 


### Problem 3: Most Useful Parts of the Course

You can highlight all of the parts of the course that you did not like in the evaluations where you are completely anonymous. Here, tell me which parts (subjects/topics) of the course you found the most useful and why. What aspects of lab or lecture most helped you learn these subjects, and how could they be made even better. (To give you perspective, each year I cut some things and add others – I want to know which things were too good to cut, and I appreciate the feedback.)