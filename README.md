# Objective of the Analysis
* Predicting whether the S&P 500 Index would have a gain for two days in a row using Classification and Supervised Learning 

# Overview of the steps involved
* Identification of dependent and independent variables
* Variable reduction – dropping variables that would not be used for the analysis
* Missing value treatment
  * For numerical variables, missing values were replaced by the mean of the variable
  * For character variables, missing values were replaced by a new categorical value “undefined”
* Feature Engineering
  * Created 3 new independent variables that were used for clustering as well as for model building
* Clustering using k means
  * 4 clusters were created after multiple iterations
* Data Visualization
* Multivariate Linear Regression Analysis
  * One multivariate linear regression model was then built for each cluster (only the final models with significant variables have been shared)

# Dependent Variable

* The variable ’target’ is the dependent variable
* It takes the value ‘Yes’ if the S&P 500 index had a gain for two days in a row and ‘No’ otherwise


# Independent Variables for Clustering and Model Building

![varsdesc](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Visualizations/varsdesc.png)

# Feature Engineering

# Data Preparation

![dataprep1_new](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/dataprep1_new.png)

![dataprep2_new](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/dataprep2_new.png)

# Decision Tree

# Random Forest

![clustering1_new](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/clustering1_new.png)


![clustering2_new](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/clustering2_new.png)

![Elbow_Curve_aug30](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Visualizations/Elbow_Curve_aug30.png)

* The Elbow Curve showed that after 6 there is a decline in the calculated sum of squared errors (SSE)
* I ran one iteration with 6 and 5 number of clusters each but in both cases 1 or 2 clusters were really small so it made sense to decrease the number of clusters
* Moreover, the elbow curve shows that there is a very negligible increase after 4 number of clusters which can be  considered insignificant.Therefore, I built 4 mutually exclusive and exhaustive clusters using k-means
* In all, 200 variables were considered for clustering



![clustersize](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Visualizations/clustersize.png)

* Cluster 3 is the biggest cluster with 75% of the rooms in it
* Cluster 1 is the smallest with just 1% of the rooms

![clustering3_new](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/clustering3_new.png)

# Visualization of the data

![v1](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/v1.png)

# Chart 1

![v2](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/v2.png)

![Chart1_aug30](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Visualizations/Chart1_aug30.png)

* Cluster 3 has the highest number of ‘Entire home/apt’ as compared to all the other clusters followed by cluster 4
* The majority of ‘Private rooms’ are in cluster 3 
* Cluster 1 has no shared rooms
* Overall, there are more number of rooms of type ‘Entire home/apt’ followed by ‘Private rooms’ 

# Chart 2

![v3](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/v3.png)

![chart2_aug30](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Visualizations/chart2_aug30.png)

* The number of rooms with moderate cancellation policy is more than the number of rooms with flexible cancellation policy for each of the clusters 1, 2 and 4 but a completely opposite trend is observed in cluster 3 
* Overall, there were almost no rooms which had a super strict cancellation policy of 30 or even 60 days

# Chart 3

![v4](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Codes/v4.png)

![chart3_aug30](https://github.com/Sonull/Unsurvised-Learning-on-Airbnb-LA-data/blob/master/Visualizations/chart3_aug30.png)

* More than 10,000 rooms in cluster 3 were not instantly bookable
* In each cluster, there are more number of rooms that cannot be booked instantly than the rooms that can be booked instantly
* This difference is least in cluster 1 followed by cluster 2 but this could also be due to the sheer size of these two clusters
