# **Problem**

I found a public dataset on AirBnB's website containing information about the numerous AirBnB rooms in New York City for the year of 2019. I decided to try and 
implement a prediction model which would help me predict the prizes of AirBnB listings in New York City for the year of 2019 
based on several geographical and availability metrics in the dataset.

# **Dataset**

Link to Dataset : https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data

Name | Description
------|----------
id | Unique identifier of each listing
name | Name of the Listing
host_name | Name of the host
host_id | Unique identifier for each host
neighborhood_group | The neighborhood cluster or city that each listing belongs to
neighborhood | The neighborhood that each listing belongs to ( A subset of neighborhood_group)
latitude | The latitude of the listing
longitude | The longitude of the listing
room_type | Private room or Entire home
Prize | Prize per day for renting the listing
Minimum_nights | Minimum nights that a customer has to rent the listing for
number_of_reviews | Number of reviews on each listing
last_review | Date of Last review on listing
reviews_per_month | Number of reviews per month on listing
calculated_host_listings_count | Number of listings per host
availability_365 | Number of days for which listing was available in the year of 2019

# Goal

The goal is to predict the listing price for any given Airbnb Listing. For example, a potential owner of a house/apartment wants to list their unit, what should they consider doing to determine their listing prices and what factors affect the prices the most?

## Exploratory Analysis:

### Scatter Plot showing Unit Listing based on longitude , latitude & Availability

![image](https://user-images.githubusercontent.com/85646063/185214531-487d88df-9665-40c4-a8b6-a0c17bedcf71.png)


### Clusters the units can be broken into:

![image](https://user-images.githubusercontent.com/85646063/185214903-42518174-e81f-41d3-9996-b390a4168df5.png)

### Listing Price Distribution

![image](https://user-images.githubusercontent.com/85646063/185215335-cb8196b7-fd7e-4e10-868f-d9247b36548a.png)

### Count of units in different neighborhoods and neighborhood groups

![image](https://user-images.githubusercontent.com/85646063/185215413-1e991a86-be74-4877-8c84-039c2fdf7df5.png)

### Histogram of Room type
![image](https://user-images.githubusercontent.com/85646063/185215487-17211abc-265a-4675-a4cb-30d6acb9740c.png)

### Scatterplot of Number of Reviews Against Price
![image](https://user-images.githubusercontent.com/85646063/185216263-91cd1ace-61f3-45be-915e-615170af33c3.png)

### Linear Regression and Feature Importance
![image](https://user-images.githubusercontent.com/85646063/185216364-8e3da9fc-0e14-449f-ad44-25aa940ef7d2.png)

![image](https://user-images.githubusercontent.com/85646063/185216388-66ce69d4-21db-4f6c-a859-c953fb5929ae.png)

### Find The Features That Have the Highest Interactions With Each Other

![image](https://user-images.githubusercontent.com/85646063/185216469-215534be-a760-4050-b0e6-8e138a3adeb9.png)

### Linear Regression After Generating Interaction Featuures

![image](https://user-images.githubusercontent.com/85646063/185216554-eef00cac-8a6c-495c-a7a4-06783abd5fe8.png)

### Gradient Boosting Regressor Results

![image](https://user-images.githubusercontent.com/85646063/185216621-a4ae4547-586e-450a-b041-271a125ef21f.png)

Gradient Boosting Regressor has the highest accuracy

## Conclusion

### Modeling Conclusions:

Originally, this model only had about 10% accuracy due to having a high number of features in the dataset. After cleaning the data, taking out outliers of the numeric features, the model's accuracy improved to about 45%. Then I engineered new features including location cluster, availability level, and whether a dataset has a high number of reviews. Also, I categorized the low frequency count neighborhoods into one category 'other.' The linear regression model's accuracy increased to 53%. Gradient Boosting Regressor was able to generate 60% accuracy.

### Additional Relevant Data Needed & Future Improvements:

There are also other factors to consider such as seasonlity, demand, number of photos that the Airbnb listing has, and the review ratings of the listings. Some of these factors are not included in this particular dataset. However, this model can also be applied to other datasets to capture more accurate results.
This project is really fun to work on. It really emphasizes the importance of feature engineering and interpreting the data before building any predictive models.
