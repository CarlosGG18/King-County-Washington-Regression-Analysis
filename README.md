# King County Washington Regression Analysis
![king-county](https://user-images.githubusercontent.com/117116368/206738892-c48bca07-f8da-4d08-81bf-e3e2c7971d56.jpeg)


This project will make use of Pandas, and NumPy, for the data exploration phase as well as using Matplotlib, Seaborn, and Folium to form visualizations. I will then be using Scikit-Learn to model my multi-variate linear regression. In order to properly account for nominal categories like zipcodes, I have One Hot Encoded into dummy variables. To properly interpret the effect of feature I have scaled the price through Log Transformations.


### Objective
#### 1 Identify features that weigh the most on home price values

* With the revaltion of features contributing the most to price home owners can inpute their own appraisals 

#### 2 Contruct Regression Model using Test-Split method to accurately make predictions

* After various models I was able to predict prices given specific features with 82% accuracy 

#### 3 Provide detailed heatmaps outlining areas with high prices

* Using Folium and Seaborn libraries I was able to construct vizualizations based off of home prices and zip codes


### Process

#### Data Cleaning

* My prcoess started with cleaning and eliminating null values as well as making sure the data was the needed data type to properly use them in my model

* The file for my data cleaning process can be found within the notebooks folder under the name Cleaning.ipynb

#### Exploritory Data Analysis (EDA)

* Process can be found in the EDA.ipynb notebook

* Once the data is cleaned I moved onto EDA which started off by exoploring  any features that correlated the heaviest heaviest compared to price, below you will find the correlation matrix made to filter out necessary features. 

![Corr_matrix](https://user-images.githubusercontent.com/117116368/206742519-6d385137-752f-446b-9e3c-794c3f104306.png)

* Outliers were removed shortly after to ensure normality of necessary features I was to include in my model (sqft_living, Grade, Zipcodes, etc.)

#### Modeling 

* After EDA I selected features with the highest correlation contribution to weight followed by a  Train-test split method to test the fit of my model and its prediction accuracy.


![image](https://user-images.githubusercontent.com/117116368/206789607-9b48ff6f-d753-4fcf-b348-794059245553.png)

My final model included OneHotEncodeding the zipcode variable given it being a nominal category with statistically significant correlation to price. The final model included (view, condition,grade, sqft_living, zipcode, and sqft_basement) with 82% prediction accuracy 

* The step by step can be found within the Modeling.ipynp notebook

#### Heatmap
To get a better understanding of which areas have the higher home prices by zipcode. Evidently the zip codes that border lake washington are the most expensive alongside Bellevue.
<img width="1552" alt="Screenshot 2023-07-20 at 5 42 43 PM" src="https://github.com/CarlosGG18/King-County-Washington-Regression-Analysis/assets/117116368/c9378161-3d4b-4bb6-86b8-9ce34c1eabf5">

* The maps were constructed using matplotlib and Folium libraries found within the HeatMap-Folium.ipynp notebooks

### Conclusion

* Although grade has a strong correlation weight with price the major contributor is focused around sqaure foot of home space alongside zipcodes. In the future I would like to subset my price data set as they have major variance in price as they range from $100K - $100M, as well as add features missing from the dataset i.e school zones. 
