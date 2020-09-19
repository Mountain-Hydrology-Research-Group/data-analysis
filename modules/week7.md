# Week 7

```note
## Lab 7: Markov Chains & Monte Carlo

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 7-1: Markov Chains](lab7/lab7-1.ipynb)
  * data: [markov_random4.txt](data/markov_random4.txt)
* [Lab 7-2: MCMC Rating Curves](lab7/lab7-2.ipynb)
  * data: [Lyell_h_Q_sorted.mat](data/Lyell_h_Q_sorted.mat)
* [Lab 7-3: Markov Chain Monte Carlo Example](lab7/lab7-3.ipynb)

```


## Homework 7: 

### Problem 1: Markov Chains

Download the spreadsheet ENSO_to2020.xls. (And yes, the current status of ENSO, neutral, is for water year 2020.) [Not required for the homework, but if you’re curious to learn more about ENSO and its impacts, see this website: https://www.climate.gov/enso ] 


 **A. **Using the time series of the phase of the El Niño Southern Oscillation (ENSO) (warm (El Nino) =1, neutral=2, cool (La Nina) =3) from 1900-2020, create a lag-1 Markov model of the ENSO phase.

 **B.** Using this Markov model and a random number generator, simulate 5,000 years of ENSO data.
    
 **C.** Using this stochastically generated data, answer the following questions. According to the model, what is the probability that three warm ENSO years would occur in a row? (Try refreshing the numbers several times to increase the sample size if the condition never happens.) What is the large-sample probability that three cool ENSO years would happen in a row?


 
### Problem 2: Application of Bayes Theorem
 
Following the Week 6 Lab, explore how the rating curve and its associated uncertainty change whether you use least squares fitting, direct monte carlo parameter estimation, or Bayesian MCMC fitting to determine the rating curve and 95% confidence intervals for the Lyell Fork streamflow site. Create plots and discuss what you did. 



### Problem 3: Statistics Synthesis (Undergraduate Students)

You are given the below dataset of annual peak flows on the Sauk River: 

 Note, you do not need to do any actual analysis here. Rather, for each of the following questions about this dataset, I want you to answer, a) How do you ask this statistically? b) What tools should you use? (Think of techniques we’ve learned in class.), and c) What should you be careful of /careful about? (Think of caveats and requirements of the tools you’re recommending).

 **A.** Presume some logging occurred in the watershed in 1970. Are peak flows higher after 1970 than before 1970?
 
 **B.** Presume some logging occurred in the watershed in 1970. Have peak flows become more variable after 1970 than before 1970?
 
 **C.** If the mean annual peak flow has increased to above 50,000 cfs, the town will rebuild the levees. What are the chances that our statistical test would fail to identify this change?
 
 **D.** Has there been a trend in peak flows between 1930 and 2010? How fast are peak flows changing, and is this trend significant?


### Problem 3: Project Update (Graduate Students)

Write out three clear (specific) questions that you are trying to answer in your project. For each question, provide 1-2 graphs that illustrate the answer to that question, as well as a couple sentences of explanation to accompany each graph (explain what you did to generate the graph, and what the graph shows). Do you think your answers are clear, or is further work needed? If you feel additional tests/analyses are needed, describe what you plan to do. If there are areas where you feel you need additional guidance, please describe the issues here. 
 
