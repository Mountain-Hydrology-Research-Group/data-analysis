
# Course Project (CEWA 565)

The goal of the course project is to give you hands on experience working with data of particular interest to you, as well as experience writing about and presenting data and statistical information. 

In your project, you will ask a question (pose a hypothesis), answer it using a variety of analysis techniques, and clearly address the statistical uncertainty of the answer. In the report, explain your objectives, your data source, your methodology, your results, and discuss remaining uncertainties.

Your project will be evaluated through an oral presentation (20% of total grade) and a written report (80% of total grade). The written report will be no longer than 10 pages (for an individual or group of two; or 15 pages for a group of three), including figures (references will not count towards the page limit).  I encourage groups of 2 (not one or three) when possible.

```{note} Additional Resources
UW has services to help people with [statistics](https://www.stat.washington.edu/consulting/) and [data analysis](https://escience.washington.edu/using-data-science/office-hours/). These are designed primarily to help graduate students engaged in research (not with homework), but presuming your course project is related to a research interest of yours, they have been very helpful in the past.
```


## Potential project ideas

You are welcome to use your own data and answer a question of interest to you and relevant to your own research. Please let the instructor know as early as possible so that we can make sure you have sufficient data to be successful. Alternatively, you may choose or adapt one of the project ideas below. Multiple groups may answer the same general question, but they should pick different specific data or specific tests to use, which can be coordinated in conjunction with the instructor. Past project examples are available on the [class Canvas page](https://canvas.uw.edu/) under *Files* > *Student Projects and Presentations* > *Project Examples*.

1. **How does forest harvesting affect flooding?** Using data from the [HJ Andrews experimental forest](https://andrewsforest.oregonstate.edu/), determine whether the risk of flooding has increased following forest harvesting. You may download timeseries data from the [class Canvas page](https://canvas.uw.edu/) or from the [HJ Andrews data page](https://andrewsforest.oregonstate.edu/data).
* Watershed 1 was a 400- to 500-year old-growth forest, measured from 1953-1961; from 1962-66, it was 100% clearcut, and in 1967, it was burned. 
* Watershed 2 was kept as a control during this time.
Using a variety of techniques we learned in class, as well as others you may encounter in the literature (use at least three different tests), determine whether forest removal increases flood risk at different return intervals in the HJ Andrews area.  What is your confidence in this (Type I and Type II errors)?  How sensitive are your results to the statistical tests you chose?

2. **How does forest regeneration (following harvesting) change summer streamflow, or low flows?** Similar to question 1, again using the HJ Andrews data.  See [Perry & Jones (2017)](https://doi.org/10.1002/eco.1790) paper on this topic. (Ask the instructor for a copy of this paper if you're unable to access it online)

**NOTE:**  For both questions 1 and 2, an error was recently found in the HJ Andrews streamflow dataset. Please read the details on their [data page](https://andlter.forestry.oregonstate.edu/data/abstract.aspx?dbcode=HF004).  In particular, Watershed 1 had streamflow change by 20% due to a recalculation of the rating curve.  The data on our class canvas page is from the old rating curve.  As one project, you may research rating curve methods, how and why they were recalculated for Watershed 1, and what impact that recalculation has on the conclusions derived from questions 1 and 2 above.  

3. **How does forest harvesting affect streamflow?**  Using data from the the [Penticon Creek Watershed](https://watersheds.ok.ubc.ca/upper-penticton-creek/), described [here](https://onlinelibrary.wiley.com/doi/full/10.1002/hyp.14391), and available [here](https://zenodo.org/records/5520109), assess how forest harvesting affects the streamflow metric of your choice.  You may address the same questions as described for the HJ Andrews watershed above, you may compare data between the two regions, or you may ask a question of your choosing.  Papers about Upper Penticon Creek are availabe under Files>Optional Reading and References>Upper Penticon Creek, on the [class Canvas page](https://canvas.uw.edu/).  In this dataset, the 240 creek is unlogged and serves as the control.  Road construction and clearcut logging began in late 1995, see papers for details. By late winter of 2007, 47% of the 241 and 52% of the Upper Dennis Creek watersheds had been clearcut.  Snow and soil moisture data, as well as lidar data for tree heights, are also available.  

4. **How does weather vary in a high-elevation valley in Colorado?**  The U.S. Department of Energy and the National Oceanographic and Atmospheric Administration have collected a lot of measurements in the East River Basin of Colorado, as part of the [SAIL and SPLASH](https://www.arm.gov/news/features/post/81524) campaigns.  The data is publicly available for both [SAIL](https://adc.arm.gov/discovery/#/results/s:guc/site) and [SPLASH](https://psl.noaa.gov/splash/). Talk to the instructor if you want to work on a project using these data. 

5. **How does stream temperature in different months and different streams relate to the onset date of snowmelt runoff (when the streams start rising)?** Elevated stream temperatures can be unhealthy for fish if snow melts earlier (resulting in earlier streamflow). You may download time series of discharge and stream temperature [here](https://www.osti.gov/dataexplorer/biblio/dataset/2324637) for different streams in Yosemite National Park, California. Using a variety of techniques we learned in class, as well as others you may encounter in the literature (use at least three different tests), determine whether stream temperature is significantly changed by streamflow timing. What is your confidence in this? You may want to consider different months of the year or different times of the day (e.g., daily maximum temperature vs. daily mean), and you may want to compare and contrast streams of different sizes. (See this [guide](https://depts.washington.edu/mtnhydr/Pages/Data/yosemite/Lundquist_2016_WRR_SupportingInfo.pdf) to learn more about these sites. Also, talk to the instructor if you want more recent data.)

6. **Does snow accumulation and/or melt change after forest disturbance?  How?** (Please ask the instructor if you’re interested in this project.)

7. **How do temperature, relative humidity, fog, and cloud cover vary across San Juan Island?  Are there potential locations of climate refugia for intertidal marine wildlife?** (Please ask the instructor if you’re interested in this project.)

8. **What variables influences groundwater at a property on the Olympic Peninsula?**  (These data are provided by a CEE alumni family, and the instructor can you in touch with them if you are interested.)

9.  **Choose your own adventure...**


## Grading Rubic


### Presentation 
(30 points; will account for 20% of project grade)

A powerpoint-type presentation, like you would present at a conference, 10 minutes in length, with an additional 5 minutes for questions. Your classmates are your audience. Present your question, why it is important, what methods you employed to answer the question, your major results, and the implications of your results. For pairs, both project partners will present together.

* Clarity of Overall Presentation (10 points)
  - Clear statement of the problem
  - Clear explanations of what you did, easy to follow
  - Good transitions from one section to the next
  - Ability to answer questions raised by audience
* Quality of Visual Aids/Graphics (10 points)
  - All graphics easy to see, properly labeled, large enough font
  - Correct limits on plot axes to show relevant information
  - Proper choice of type of graph to convey information
  - Interest level – slides nice/interesting to engage audience
* Technical Analysis and Discussion (10 points)
  - Proper methods applied
  - Accuracy of results
  - Explanation of why results are what they are
  - Ability to relate results to other studies and other presentations in the class


### Written Report
(30 points; will account for 80% of project grade)

For the written report, you must include an abstract (no more than 300 words) and a list of references; these can be in addition to your 10 (for a group of two; or 15 for a group of three) pages.  Follow the same format outlined for the presentation but feel free to include more details (equations, etc.). Please address any questions or comments that were raised during the presentation. Use clear, concise sentences and proper grammar.

* Quality of Writing (10 points)
  - Clear and easy to read 
  - Proper grammar and spelling
  - Clear statement of the problem 
  - Good transitions from one section to the next
  - Clarity of explanations of what you did
* Technical Analysis (10 points)
  - Clearly described methods, proper literature cited
  - Technical difficulty of methods applied
  - Accuracy of results
* Interpretation, Analysis, and Discussion of Result (10 points)
  - Attempted to explain why certain patterns were observed in the data and/or analysis 
  - Thought about results in context of other studies
  - Outlined next steps to be taken
  - Addressed underlying assumptions in the analysis and how these may have affected results
