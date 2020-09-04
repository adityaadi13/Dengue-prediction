# Dengue-prediction

Question statement - Using environmental data collected by various U.S. Federal Government agencies—from the Centers for Disease Control and Prevention to the National Oceanic and Atmospheric Administration in the U.S. Department of Commerce—can you predict the number of dengue fever cases reported each week in San Juan, Puerto Rico and Iquitos, Peru?

Before looking into the data set, I did some initial analysis about temperature dependence on mosquito breeding rate, and on dengue virus - to find out that both of the cities posses the conditions for mosquitoes to thrive.
![Where does it thrive?](https://github.com/adityaadi13/Dengue-prediction/blob/master/Images/1.PNG)

## Looking at EDA we find interesting insights:
Important factors for San Juan that affect the number of dengue cases are different from Iquitos - meaning that it is critical that we make different models for them!
![San Jose EDA?](https://github.com/adityaadi13/Dengue-prediction/blob/master/Images/3.PNG)
![Iquitos EDA](https://github.com/adityaadi13/Dengue-prediction/blob/master/Images/4.PNG)


## Game plan:
Now that we understand that it is important to make different models, it is time for pre-processing the data to make it more suitable for analysis. One of the main challenges was to impute the missing values - as with any dataset. As the number of cases has seasonal variation (mostly - monthly), I used monthly averages over the years. Example -  if a value in Feb'18 is missing, I took average from other years during the month of February. There were other considerations like this as well. The picture below enlightens the game plan that I will follow:
![Iquitos EDA](https://github.com/adityaadi13/Dengue-prediction/blob/master/Images/5.PNG)

## Results and Final Models:
We used Mean Absolute Error to calculate the error in our models and to pick the best. For San Juan, we find that Lasso regularised Gradient Boosting works the best with an MAE of 11.16. For Iquitos however, Gradient Boosting is the most promising with test set MAE of 5.63.

![San Juan - result](https://github.com/adityaadi13/Dengue-prediction/blob/master/Images/6.PNG)
![Iquitos - result](https://github.com/adityaadi13/Dengue-prediction/blob/master/Images/7.PNG)


