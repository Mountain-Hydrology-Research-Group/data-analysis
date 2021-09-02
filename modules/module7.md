# 7) Markov Chains

```note
## Lab 7: Markov Models & Markov Chain Monte Carlo (MCMC)

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 7-1: Markov Chains - Basic Examples](lab7/lab7-1.ipynb)
  * data: [markov_random4.txt](data/markov_random4.txt)
* [Lab 7-2: Markov Chain - ENSO Phases](lab7/lab7-2.ipynb)
  * data: [ENSO_to2021.csv](data/ENSO_to2021.csv)
* [Lab 7-3: MCMC Rating Curves](lab7/lab7-3.ipynb)
  * data: [Lyell_h_Q_sorted.mat](data/Lyell_h_Q_sorted.mat)

```


## Homework 7: 

 
### Problem 1: Application of Bayes Theorem with MCMC
 
Following the Lab 7-3, explore how the rating curve and the 95% confidence intervals for the Lyell Fork streamflow site change depending on the method you use:

- Least squares linear regression fitting (with transformed variables) using h0 = 28 cm
  - Make 95% confidence intervals around this regression fit 
  - Then, assume that we don't know exactly what h0 is. Try additional linear regressions using different values of h0 = 10, 20, 30, 40, and 50 cm (you do not need to calculate 95% confidence intervals for these additional fits)
  - Qualitatively, is the range between these 5 additional lines with different h0 values larger or smaller than the range between the 95% confidence lines from the original fitted line (the one with h0 = 28 cm)?
- Direct monte carlo parameter estimation
- Bayesian MCMC fitting

Create plots and discuss the differences in the results from these three methods.

### Problem 2: Air Temperature Observations in Complex Terrain

[See problem 2 in Module 8](/data-analysis/modules/module8.html)


### Problem 3: Statistics Synthesis (CEE 465)

You are given the below dataset of annual peak flows on the Sauk River: 

![Sauk River Plot](lab7/sauk-river-plot.png)

(Note, you do not need to do any actual analysis here)

For each of the following questions about this dataset, I want you to answer:
 - How do you ask this question statistically? 
 - What tools should you use to answer this question? (think of techniques we’ve learned in class)
 - What should you be careful about? (think of caveats and requirements of the tools you’re recommending).

 **A.** Presume some logging occurred in the watershed in 1970. Are peak flows higher after 1970 than before 1970?
 
 **B.** Presume some logging occurred in the watershed in 1970. Have peak flows become more variable after 1970 than before 1970?
 
 **C.** If the mean annual peak flow has increased to above 50,000 cfs, the town will rebuild the levees. What are the chances that our statistical test would fail to identify this change?
 
 **D.** Has there been a trend in peak flows between 1930 and 2010? How fast are peak flows changing, and is this trend significant?