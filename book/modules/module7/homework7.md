# Homework 7

 
## Problem 1: ENSO Phases
Following Lab 7-1 and Lab 7-2,

**A.** *(1)* Use the time series of the phase of the El Niño Southern Oscillation (ENSO) from 1900-2022 to create a lag-1 Markov model of the ENSO phase, where the observed Phases of ENSO are as follows:

1. warm (El Niño)
2. neutral (ENSO neutral)
3. cool (La Niña)

**B.** *(2)* Using this Markov model and a random number generator, simulate 5,000 years of ENSO data. Then answer the following questions.

  - According to the model, what is the probability that three warm ENSO years would occur in a row?
  - What is the large-sample probability that three cool ENSO years would happen in a row?  (Try refreshing the numbers several times to increase the sample size if the condition never happens.)

Check out this [blog](https://www.climate.gov/news-features/blogs/september-2022-la-ni%C3%B1a-update-it%E2%80%99s-q-time) about why we care about ENSO and the exciting current probability of getting a cool ENSO (La Nina) again in 2023, making it three in a row.

## Probelm 2: Rating Curves and Application of Bayes Theorem with MCMC
 
Following the class discussion and Lab 7-3, explore how the rating curve and the 95% confidence intervals for the Lyell Fork streamflow site change depending on the method you use to determine the rating curve:

**A.** *(2)* Least squares linear regression fitting (with transformed variables) using b = 0.28 m
  - Make 95% confidence intervals around this regression fit
  - Then, assume that we don't know exactly what b is. Try additional linear regressions using different values of b = 0.10, 0.20, 0.30, 0.40, and 0.50 m (you do not need to calculate 95% confidence intervals for these additional fits)
  - Qualitatively, is the range between these 5 additional lines with different b values larger or smaller than the range between the 95% confidence lines from the original fitted line (the one with b = 0.28 cm)?
  
**B.** *(1.5)* Direct monte carlo parameter estimation

**C.** *(1.5)* Bayesian MCMC fitting

Using the code in Lab 7-3, create plots and discuss the differences in the results from these three methods. *(2)*

