# Week 6


```note
## Lab 6: Bayesian Statistics

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 6-1: Bayesian Statistics](lab6/lab6-1.ipynb)

```


## Homework 6: 

### Problem 1: A Bayesian Example

A medical testing company has developed a two-stage, non-invasive test for Down’s syndrome in the first two months of pregnancy. Initial tests have shown that when the fetus actually has Down’s syndrome, the test correctly identifies this by giving a positive result 98% of the time (i.e. the observed probability of a false negative is 2%). Furthermore, in cases when the fetus does not have Down’s syndrome, the test result is negative 97% of the time (i.e. the observed probability of a false positive is 3%). Armed with this data, the company’s statisticians are charged with estimating the overall probability that a given fetus has Down’s syndrome if the test shows positive. Assume the observed probability of Down’s syndrome in a random sample from a large number of observations is about 1 in 1,200 (this is the reported value for a 25-year-old mother; the risk is higher for older mothers).

 **A.** Using Bayes’ theorem, estimate the overall probability that a given fetus has Down’s syndrome if the test shows positive. Are you surprised by the answer? What is the fundamental problem with this test? How accurate would the test have to be to achieve a 50% probability of having the disease if the test showed a positive result? (For the last one, experiment with the accuracies of both the positive and negative test results.)

 **B.** Estimate the likelihood that the fetus does not have Down’s Syndrome if the test shows a negative result. Is the test more useful in this framework as a screening step when trying to decide to use more accurate (but also more invasive) tests?
    
 **C.** Finally, draw a tree diagram for this problem.

 
### Problem 2: Continuous Bayesian Estimation of Flood Frequency
 
Based on long-term climate records, the 24-hour duration, 100-year return period rainfall in New York City was previously estimated at 7.2 inches. 100-year rainfall indicates a storm with a rainfall total that would on average be met or exceeded only once every 100 years. In a given year, the storm has a 0.01 chance of occurrence, i.e., for any k-year storm, its probability of occurrence in one year is 1/k, where k is the return period. In fact, during the 20th century, this total was exceeded only once, during Hurricane Floyd in 1999. However, a storm in 2007 produced 8 inches of rainfall in a 24-hour period. Another storm in August 2011 again exceeded the 7.2-inch total. Hurricane Irene in September 2011 exceeded the total yet again, and so did Hurricane Sandy in October 2012. This happened again in September 2018 from Hurricane Florence. 

```note
Note that in 2019, there was flooding in July, but not of this magnitude. Also, subtropical Storm Melissa brought minor flooding to the New York coastline on 11 October 2019 but not of this magnitude. Therefore, we will not update the number of floods in 2019 but will instead add one more year without a flood.
```

In this problem we will use Bayes’ Theorem to estimate the probability that the 7.2-inch storm is no longer the 100-year storm, that is, the probability that 7.2 inches of rainfall in a 24-hour period is likely to occur more often than every 100 years. In this problem, A is the true likelihood of the storm’s occurrence, and B are the events we have observed. 

```note
Note that unlike what you will do in many hydrology classes, which is to calculate the return period across a range of different precipitation or streamflow values, we are focusing here only on the probability of 24-hour storms exceeding 7.2 inches of rainfall because this is a critical design number for New York City.
```

 **A.** Download and plot the prior likelihood of a >=7.2-inch storm occurring in a given year from the data file “NYC_precip_priors” (.xslx or .mat). This dataset shows the prior distribution of the likelihood of the 7.2-inch storm in a given year, with mean p = 0.01. Note that the variable labeled “pdf” represents the probability of the storm frequency or return interval falling within that interval (value noted and the next value) and therefore includes the interval width, such that the sum of the pdf values alone sums to 1, and cumulative sum of the pdf is the cdf. Note that there is some uncertainty about the original likelihood. What are the mean and 95% confidence interval of the probability, i.e., where does 95% of the PDF fall between? To what k-year storm (expected return period) range do these values correspond?

 **B.** At each time period of interest, count the number of times the threshold has been exceeded and the number of years, beginning with the period 1900-1999. The likelihood P(B|A = p) that the storm would be exceeded m times in n years (event B) for a storm probability p (event A = p) is given by:

P(B|A = p) = binomdist(m,n,p)

 Calculate the posterior likelihood of the 7.2-inch storm’s probability after the period 1900-1999, which includes only Hurricane Floyd. Use the continuous version of Bayes’ Theorem to calculate the probability of A at all values of p. What are the mean and the 95% confidence interval of the return period for the 7.2-inch storm after 1999?
    
 **C.** Now update the posterior likelihood of the storm’s probability by considering the period from 2000-2010 (storm 2), and then the period 2011-2019 (storms 3, 4, 5, and 6). Remember to change the number of storms (m) and the number of years (n) at each step. Use the previous step’s posterior distribution as the new prior distribution at each step, and update only with the new years. Plot the posterior distributions after each update, and state the mean and 95% confidence interval of the return period each time (as in B but for the updated distributions).
    
 **D.** How much did the mean and 95% confidence interval return period change from the original prior return period to 2019? What does this indicate about the “true” frequency of the 7.2-inch-storm?






