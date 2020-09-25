# STOCK ANALYSIS REFACTORING
## OVERVIEW
The purpose of this analysis is to determine the value of refactoring code using an analysis of Stock Market data as a test case. 
### BACKGROUND
Steve wants to know if the code developed to analyze a small set of stocks can be optimized to use on the whole stock market.  Consideration must be given to whether the code can be refactored in order to speed up the processing of the data. 
## ANALYSIS
In order to see if refactoring the code used to analyze 12 stocks can help optimize the performance of the code to make it compatible with running it on the whole stock market, a comparison of the code before refactoring and after has been done.  

Steve was interested to know about the performance of a group of 12 stocks in 2017 and 2018.  The first run of code results in the following stock tickers results and the associated run time for the code:

![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/Orig%202017.PNG)
![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/2017%20incl%20formatting%20before.PNG)


![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/Orig%202018.PNG)
![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/2018%20formatting%20before.PNG)

After Refactoring the code the stock market analytic results are the same but the timing has changed as shown below:

![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/2017%20challenge%20results.PNG)
![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/2017%20challenge.PNG)

![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/2018%20Challenge%20Results.PNG)
![alt text](https://github.com/xactuary/Stock-Analysis/blob/master/Resources/2018%20challenge.PNG)

Clearly the run time has been reduced substantially by making some changes to the code.
