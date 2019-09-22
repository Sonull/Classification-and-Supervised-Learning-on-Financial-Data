# Objective of the Analysis
* Predicting whether the S&P 500 Index would have a gain for two days in a row using Classification and Supervised Learning 

# Dependent Variable

* The variable ’target’ is the dependent variable
* It takes the value ‘Yes’ if the S&P 500 index had a gain for two days in a row and ‘No’ otherwise

# Independent Variables 

![table1](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/table1.png)

# Feature Engineering

* Created the following new independent variables for Visualization and Classification

![table2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/table2.png)

# Visualization of the data

# Chart 1

![chart1](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart1.png)

![graph1](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph1.png)

* The difference between the High and Low Price of the Stock is lowest on Wednesday
* The difference between High and Low price is more than 100$ usually on a Monday and Thursday

# Chart 2

![chart2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart2.png)

![graph2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph2.png)

* The difference between Close Price and Open Price is more spread out during the first month and the last month
* The trading activities seem to be affected by seasonality
* The fluctuations are the lowest in Quarter 3. Here Quarter 3 is the period from month 7 through 9

# Chart 3

![chart3](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart3.png)

![graph3](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph3.png)

* The Percentage difference between the High Price and the Open Price is the highest during the months 1 and 12
* Usually, the percentage difference between the High Price and Open price is less than 5%, for any month
* For the month 1, the high price of a day went up as high as 10% from the open price

# Chart 4

![chart4](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart4.png)

![graph4](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph4.png)

* The distribution of the difference between the High Price and Low Price is majorly concentrated around 15$ for years 1 and 2
* This difference is seen to be getting more spread out across the years, that is the variability has been seen to increase down the years
* For a majority of the years, the difference seems to be concentrated around 25$. This means usually, the value of the high price is not more than 25$ than low price throughout the year
* This chart basically tells us that the stock market is very volatile and each year the difference between High Price and Low Price fluctuates a lot

# Chart 5

![chart5](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart5.png)

![graph5](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph5.png)

* The Percentage difference between Open Price and Low price has been the lowest for month 12, with the low price being even less than 7.5% than the Open Price
* Usually the Percentage of difference between the Open Price and Low Price is within 5% 

# Chart 6

![chart6](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart6.png)

![graph6](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph6.png)

![eight](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/eight.png)

![graph7](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph7.png)

 * There exists a positive linear relationship between the Low Price of the stock and the Close Price of the stock
 * As the Low Price increases the Close Price is expected to increase
 * This is evidenced by the overall data as well as the data for each year  

# Chart 7

![chart7](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/chart7.png)

![graph8](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph8.png)

![nine](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/nine.png)

![graph9](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/graph9.png)

 * There exists a positive linear relationship between the High Price and the Close Price
 * As the High Price increases the Close Price is expected to increase
 * This is evidenced by the overall data as well as the data for each year  

# Decision Tree

![dp1](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dp1.png)

![dp2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dp2.png)

![dp4](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dp3.png)

![dtree-iteration2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Visualization/dtree-iteration2.png)

* The first node tells the split between Yes and No in the original data which is 28% and 72% respectively 
* The variables that were identified as significant initially were:
  * changenet_same 				
  * changepct_same  
  * ChangePercent.1 
  * open_to_high_net 
  * open_to_high_pct  
  * open_to_low_net  
  * open_to_low_pct     
  * RangeNet    
  * RangePercent  
  * RangePercent.1  
* The variables that were finally in the model because of their significance are:
  * ChangePercent.1 
  * if the percentage change in the Open and Close Price for the previous day is less than -0.005, then there is 46% probability that the S&P 500 Index would NOT have a gain for two days in a row 
changenet_same
  * if the percentage change in the Open and Close Price for the previous day is NOT less than -0.005  AND if the net change between Open and Close Price for the same day is < 0.13 then there is a 28% probability that the S&P 500 Index would have a gain for two days in a row 

![dtree1](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dtree1.png)

![dtree2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dtree2.png)

![dtree3](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dtree3.png)

![dtree4](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dtree4.png)

![dtree5](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/dtree5.png)

* True positives = 240
* True negatives = 640
* False positives = 11
* False negatives = 10
* Therefore, accuracy of the model = (True positives + True Negatives)/ Total
		                                 = (240+640)/901
		                                 = 0.97669
		                                 ~ 98%


# Random Forest

![randomforest](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/randomforest.png)

![rff1](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/rff1.png)

![rff2](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/rff2.png)

* According to the Mean Decrease in Gini Value the top five most significant variables in predicting whether the S&P 500 index would have a gain two days in a row are:
  * ChangePercent.1
  * changenet_same
  * changepct_same
  * open_to_low_net
  * open_to_low_pct
  
![rff3](https://github.com/Sonull/Classification-and-Supervised-Learning-on-Financial-Data/blob/master/Codes/rff3.png)

* The accuracy of the model  = (242+642)/total * 100 
		             = 98.11%
			     





