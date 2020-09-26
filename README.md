# STOCK ANALYSIS REFACTORING
## OVERVIEW
The purpose of this analysis is to determine the value of refactoring code using an analysis of Stock Market data as a test case. 
#### BACKGROUND
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

Clearly the run time has been reduced substantially by making some changes to the code but getting the same results.  

### DISCUSSION OF REFACTORING
Refactoring the code can help a project by taking fewer steps, using less memory, or improving the logic of the code to make it easier for future users to read.  
In the stock analysis code, instead of using variables as counters to accumulate the volume, the refactored code uses arrays to capture the values for output.  
According to EDUCBA.com 
>one of the major advantages of an array is that they can be declared once and reused multiple times. It represents multiple values by making use of a single variable. This helps in improvement of reusability of code and also improves the readability of the code.

Whereas in the original code, an array was used for the stock tickers, the refactored code now includes arrays for the output variables. 

The variables before refactoring
```
Dim startingPrice As Single
Dim EndingPrice As Single
```
This compares to the array used after refactoring
```
Dim tickerVolumes(12) As Long
Dim tickerstartingPrices(12) As Single
Dim tickerendingPrices(12) As Single



