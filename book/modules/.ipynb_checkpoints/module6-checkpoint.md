# 6) Bayesian Statistics


```note
## Lab 6: Bayesian Statistics

**Lab 6-1: A Bayesian Example**

A medical testing company has developed a non-invasive test for Down’s syndrome in the first two months of pregnancy. This test can correctly identify Down’s syndrome by giving a positive result 98% of the time (true positive). Therefore the probability of a false negative is 2%. This text can correctly identify when the fetus does not have Down’s syndrome by giving a negative result 97% of the time (true negative). Therefore the probability of a false positive is 3%. For this example, assume that the observed probability of Down’s syndrome in a random sample from a large number of observations is about 1 in 1,200.

 **A.** Draw a tree diagram for this problem as you work through this example.

 **B.** Using Bayes’ theorem, estimate the probability that a fetus has Down’s syndrome given that the test result is positive. Are you surprised by the answer? What is the fundamental problem with this test?
 
 **C.** How accurate would the test have to be to achieve a 50% probability of having Down’s syndrome given that the test result is positive (true positive)? (**Note**: In this problem, try solving for the accuracies of both the positive and negative test results that will give you a 50% true positive rate. It may not be possible to achieve a 50% true positive rate with one or the other.)

 **D.** Estimate the likelihood that the fetus does not have Down’s Syndrome given that the test result is negative (true negative). Is the test more useful in this framework as a screening step when trying to decide to use more accurate, but also more invasive, tests?
    
---

Download the lab and data files to your computer. Then, upload them to your JupyterHub [following the instructions here](/resources/b-learning-jupyter.html#working-with-files-on-our-jupyterhub).

* [Lab 6-2: Bayesian Statistics](lab6/lab6-2.ipynb)

```


## Homework 6: 

### Problem 1: Continuous Bayesian Estimation of Flood Frequency

The "[100 year storm](https://en.wikipedia.org/wiki/100-year_flood)" is a storm with a rainfall total that would on average be met or exceeded only once every 100 years, and therefore the storm has a 0.01 chance of occurrence each year. For any "k-year storm", its probability of occurrence in one year is 1/k, where k is the return period in years. Infrastructure is often designed to handle the flooding due to some k-year storm.
 
Based on long-term climate records for New York City, the 24-hour duration, 100-year return period rainfall was previously estimated at 7.2 inches. This "7.2 inches in 24 hours" storm (the "100 year storm") has been used to design infrastructure in New York City. When this design limit is exceeded, flooding can occur.  

During the 20th century, this limit was exceeded only once, during Hurricane Floyd in 1999. However, a storm in 2007 produced 8 inches of rainfall in a 24-hour period. Another storm in August 2011 again exceeded 7.2 inches in 24 hours. Hurricane Irene in September 2011 exceeded this limit yet again, and so did Hurricane Sandy in October 2012. This happened again in September 2018 from Hurricane Florence, and then Hurricane Ida broke rain records in September 2021. Fortunately, this limit was not exceeded in 2022. The table below summarizes the time periods and the number of times this design limit was exceeded within each time period.

Note that, unlike what you will do in many hydrology classes, which is to calculate the return period across a range of different precipitation or streamflow values, we are focusing here only on the probability of 24-hour storms exceeding 7.2 inches of rainfall because this is a critical design number for New York City.  If you are interested in city planning in New York around floods, they released a [design plan](https://www1.nyc.gov/assets/orr/pdf/publications/stormwater-resiliency-plan.pdf) in May 2021.  Note they use different rain thresholds for different design elements (e.g., sometimes hourly rain rates matter more), so the actual critical design numbers vary more than what we're examining here.  You may also be interested in reading recent news about this problem.  One from [NPR](https://www.npr.org/2022/10/29/1131608305/a-decade-after-sandy-hurricane-flood-maps-reveal-new-yorks-climate-future) and one from the [New York Times](https://www.nytimes.com/2022/10/21/realestate/sandy-hurricane-ida-flooding.html).  The news articles are not required reading to do the homework.  

| time period | # of years | # of storms |
| --- | --- | --- |
| 1900-1999 | 100 | 1 |
| 2000-2009 | 10 | 1 |
| 2010-2019 | 10 | 4 |
| 2020-2022 | 3  | 1 |

In this problem we will use Bayes’ Theorem to see if the 7.2-inch storm is still a 100-year storm. In other words, we want to find what k-year storm 7.2 inches in 24 hours corresponds to, if not 100-years.

 **A.** Download and plot the prior pdf of a >=7.2-inch storm occurring in a given year from the data file [NYC_precip_priors.csv](data/NYC_precip_priors.csv). This dataset shows the prior distribution of the chance that New York City will get a 7.2-inch storm in a given year, which has a mean p = 0.01, corresponding to 100 years (1/p = 1/0.01 = 100). 
 
(Note that the variable labeled “PDF” represents the probability of the storm frequency (or return period) falling within that interval and therefore includes the interval width, such that the sum of the pdf values alone equals 1, and the cumulative sum of the pdf is equal to the cdf.)
 
There is some uncertainty about the original likelihood, so we want to determine: 
   - What are the mean and 95% confidence interval of the probability, i.e., where does 95% of the PDF fall between? 
   - To what k-year storm (expected return period) range do these values correspond?

**B.** Apply Bayes' Theorem at each time period of interest (see table above) to update the the pdf for the 7.2-inch storm.

P(A\|B) = P(B\|A) * P(A) / P(B)
 
In this problem, A is the true likelihood of the storm’s occurrence, and B are the events we have observed. For the first time peirod, use the pdf from the data file as the prior pdf, P(A). For each subsequent time period, use the posterior pdf from the previous time period. The likelihood P(B\|A = p) that the storm would be exceeded m times in n years (event B) for a storm probability `p` (event A = p) is given by: P(B\|A = p) =  `scipy.stats.binom.pmf(m,n,p)`, where `m` is the number of storms, and `n` is the number of years.
   - Calculate and plot the posterior pdfs of the 7.2-inch storm’s probability after each time period.
   - Calculate the the mean and 95% confidence interval of the return period each time.
    
 **C.** How much did the mean and 95% confidence interval return period change from the original prior return period to 2021? What does this indicate about the “true” frequency of the 7.2-inch-storm? To what k-year storm does this mean correspond to now?


### Problem 2: Project Update (CEWA 565)

Provide an update on your term project. By now you should have acquired all of the data you need for your term project.

 **A.** Create 2-3 plots that illustrate your data. These can be time-series plots, histograms, CDFs, whatever is relevant to your data and your problem.
    
 **B.** Discuss the quality of your data. Do you need to take into account any erroneous values or uncertain numbers before you start your statistics?
    
 **C.** Write down at least two very specific questions that you will answer with your data. For each question, write down which statistical tools you will use to help answer it.
    
 **D.** Based on what you have so far, do you think that your project scope is about right for a 10 page paper, or do you feel that you need to either simplify things to make it shorter or add complexity to make it longer? If you feel adjustments are needed, how to you plan to address this issue?
    
 **E.** What do you anticipate being the most difficult parts of your term project? Do you have questions you would like help with or advice on? Write them here.