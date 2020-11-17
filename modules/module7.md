# 7) Markov Chains

```note
## Lab 7: Markov Chains & Monte Carlo

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 7-1: Markov Chains - Basic Examples](lab7/lab7-1.ipynb)
  * data: [markov_random4.txt](data/markov_random4.txt)
* [Lab 7-2: Markov Chain - ENSO Phases](lab7/lab7-2.ipynb)
  * data: [ENSO_to2021.csv](data/ENSO_to2021.csv)
* [Lab 7-3: MCMC Rating Curves](#)
  * data: [Lyell_h_Q_sorted.mat](data/Lyell_h_Q_sorted.mat)

```


## Homework 7: 

 
### Problem 1: Application of Bayes Theorem
 
Following the Week 7 Lab, explore how the rating curve and its associated uncertainty change whether you use least squares fitting, direct monte carlo parameter estimation, or Bayesian MCMC fitting to determine the rating curve and 95% confidence intervals for the Lyell Fork streamflow site. Create plots and discuss what you did. 

### Problem 2: Air Temperature Observations in Complex Terrain

(from module 8)


### Problem 3: Statistics Synthesis (CEE 465)

You are given the below dataset of annual peak flows on the Sauk River: 


 Note, you do not need to do any actual analysis here. Rather, for each of the following questions about this dataset, I want you to answer, a) How do you ask this statistically? b) What tools should you use? (Think of techniques we’ve learned in class.), and c) What should you be careful of /careful about? (Think of caveats and requirements of the tools you’re recommending).

 **A.** Presume some logging occurred in the watershed in 1970. Are peak flows higher after 1970 than before 1970?
 
 **B.** Presume some logging occurred in the watershed in 1970. Have peak flows become more variable after 1970 than before 1970?
 
 **C.** If the mean annual peak flow has increased to above 50,000 cfs, the town will rebuild the levees. What are the chances that our statistical test would fail to identify this change?
 
 **D.** Has there been a trend in peak flows between 1930 and 2010? How fast are peak flows changing, and is this trend significant?