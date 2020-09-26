# STOCK ANALYSIS REFACTORING
## OVERVIEW
The purpose of this analysis is to determine the value of refactoring code using an analysis of Stock Market data as a test case. 
#### BACKGROUND
Steve wants to know if the code developed to analyze a small set of stocks can be optimized to use on the whole stock market.  Consideration must be given to whether the existing code can be refactored in order to speed up the processing of the data. 
## ANALYSIS
In order to see if refactoring the code used to analyze 12 stocks can help optimize the performance of the code to make it compatible with running it on the whole stock market, a comparison of the code before and after refactoring has been done.  

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

Clearly the run time has been reduced substantially by making some changes to the code but getting the same results. The only change to the output was removing the $ from the Total Volume in the refactored code.    

#### DISCUSSION OF REFACTORING
The advantage of refactoring the code is that taking the time to do this can help create a program that takes fewer steps, uses less memory, or improves the logic of the code to make it easier for future users to read. The first attempt at writing code to accomplish a task may not be the most efficient method to get the job done but it may work and get the answer right away.  The disadvantage of refactoring the code is that it takes additional time.  Many projects may require a quick turn around and don't require efficiency to get the results. In these cases, it might not be worthwhile to spend the time refactoring the original code.  However, if the project is going to put code into production that will be reused by many people or run on very large datasets, it is important to refactor it to make sure it is efficient and correct for all cases. Some programmers may decide it is easier to start over from scratch than to refactor someone else's code. 

#### REFACTORING APPLIED TO THE STOCK ANALYSIS
In the stock analysis code, Steve wants to be able to use the code on a much larger dataset.  This means that the code needs to be as efficient as possible.  To accomplish this, instead of using variables as counters to accumulate the volume, the refactored code uses arrays to capture the values for output.  

According to EDUCBA.com 
>one of the major advantages of an array is that they can be declared once and reused multiple times. It represents multiple values by making use of a single variable. This helps in improvement of reusability of code and also improves the readability of the code.

Whereas in the original code, an array was used for the stock tickers only, the refactored code now also includes arrays for the output variables. 

The variables before refactoring
```
Dim startingPrice As Single
Dim EndingPrice As Single
TotalVolume=0
```
This compares to the array used after refactoring
```
Dim tickerVolumes(12) As Long
Dim tickerstartingPrices(12) As Single
Dim tickerendingPrices(12) As Single 
```
Another item in the refactoring that was changed is the equation for checking to see if the ticker has changed in order to pull the starting and ending prices.  The equation was simplified to make it easier to follow and improve efficiency.  The original code used was
```
If Cells(j,1).Value = ticker and Cells(j-1,1).Value <> ticker then startingPrice=Cells(j,6).Value
```
This code included the "and" statement to look at both the current value and the value before.  The updated code simplifies the equation just to compare the current value to the prior value:
```
If Cells(j, 1).Value <> Cells(j - 1, 1).Value Then tickerstartingPrices(tickerindex) = Cells(j, 6).Value
```
Both methods require the data to be sorted by Column 1.  The new method reduces the complexity of the code and speeds up the processing by removing the "and" step.  

## CONCLUSION
The benefit of refactoring the code for the Stock Analysis is apparent in the significant decrease in time needed to run the code.  However, the cost of refactoring is the additional amount of time it takes to comb through someone else's code to both understand it and then make improvements upon it.  Starting with someone else's code may be more difficult then just starting over with new code.  The value of refactoring has to do with how the end project will be used.  If someone just needs a quick answer to a question, then the code efficiency doesn't matter as much as if someone needs to have code that can be implemented and reused by other people or on larger datasets.  The addition of using arrays and a simple change to an equation on the stock analysis is a small refactoring change and should benefit the use of the code on the whole stock market dataset.  


 




