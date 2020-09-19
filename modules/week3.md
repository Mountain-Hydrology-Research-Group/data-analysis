# Week 3


```note
## Lab 3: ANOVA and Regression

Download the lab file to the same folder you created in Lab 1 (the data file is the same one used in Lab 1.1, and you do not have to download it twice but it is provided here again). Then, open the lab file using Jupyter Notebook and follow the directions.

 * Lab 3.1 (.ipynb) ANOVA [preview]
   * data: ANOVA_fertilizer_treatment.txt
 * Lab 3.2 (.ipynb) Regression [preview]
   * data: pillows_example.csv
 * Lab 3.3 (.ipynb) Quantile Regression Modeling [preview]
 * Lab 3.4 (.ipynb) Confidence Intervals [preview]


```



## Homework 3: 

### Problem 1

Download the HJ Andrews Peak Flow data below to the folder you created for this class in Lab 1.0. 

For this problem, consider only differences between WS1 and WS2. These two watersheds are adjacent to each other, and we expect they experience the same storms leading to peak runoff. WS2 is the control, but WS1 was actively 100% clearcut from late 1962 to 1966. Here we want to test whether the difference in peak flows between WS1 and WS2 is statistically different in 4 periods (labeled Index12), where 1 indicates the control period pre-treatment, 2 indicates the period of active treatment, 3 indicates the first 15 years post-treatment (when the forest would start to recover), and 4 indicates longer than 15 years post-treatment. We want to know whether the four periods are statistically different from each other, and if so, which one or ones are statistically different from which other ones.

 **A.** First, plot the timeseries of peakflow as a function of wateryear for both watershed 1 and watershed 2 on the same graph, with vertical dashed lines to indicate the different periods (put a vertical dashed line in 1963, in 1967, and in 1982).
 
 **B.** It has been suggested that paired data such as this can be made to be closer to normally distributed by taking the log of each value before subtracting. Create two series: Q12=Peakflow1-Peakflow2; and Qlog12=log(Peakflow1)- log(Peakflow2); and make graphs to demonstrate which is closer to normally distributed. Given that we want to use an ANOVA analysis, why is it important to do a transformation to get the data closer to normally distributed?
 
 **C.** State the null and the alternative hypothesis for the question of whether the four periods are statistically different from each other. State the type I error (alpha value) that you are willing to accept.
 
 **D.** Perform an ANOVA test and discuss the results, related both to your hypothesis test listed above and to the more detailed question of which groups are statistically different from which other groups. Include graphs and/or tables that illustrate your results, and be sure to discuss what they mean. It's fine to use computer software here, but be sure that you understand what the code is doing and outputting.
 
### Problem 2
 
Download the Dalles peak flow data below to the folder you created for this class in Lab 1.0. 
 
USGS gaged streamflow records for the Columbia River at The Dalles, OR began in 1878 and continues to the present day (one of the longest continuous records in the U.S.). Peak flow records (based on peak stage values recorded by railroad workers), however, extend back even farther, to 1858. Using coincident peak flow records from 1879-1932 (a period with no major storage dams on the Columbia):

 **A.** First, isolate the period of relevant overlap (1879-1932) and plot the timeseries. Create a regression model for annual flow using spring peak flow as an explanatory variable.
 
 **B.** How much of the variance is explained by the resulting model?
 
 **C.** Estimate the 95% confidence bounds for the annual flow estimates from 1858- 1877, and plot them with the central tendency (the prediction from the regression model).
 
 **D.** Now create a non-parametric, quantile-based regression model using the same data.
 
 **E.** Plot the predictions and residuals for the two different prediction models for the training period (1879-1932) and plot the model predictions for the pre-1878 data for the two different models. Is there a substantial difference between the two model formulations?
 
