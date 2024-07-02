
HEART DISEASE
-----------------------------------------------------------------------------------------------------
Someone dies from Heart Disease every 33 seconds, every 1 in 5 deaths is realted to Heart Disease. 
This is a huge number! From the high number of deaths people have changed diets, exercise routines and 
even monitor their metrics through a watch. Our project is about Heart Disease predciting the future of 
this disease and what the figure will be in the future. Our Linear Regression Model should show the 
characteristics of a higher chances of developing this disease. 

Our project starts off with EDA. We imported our csv file, "Disease_Data.csv" from (from what website) 
we broke this down to Race, Age, General and Overall. Next the is seeing the years of our dataset which 
starts in 2000 to 2020. After cleaning the data our final DataFrame is pictured below:

![](Images/dataframe.PNG)

After getting our DataFrame clean we move on to breaking up the columns by our topics; Age, Gender,
Race, and Overall. Export these filtered DataFrames into separate csv files, this was to cut down the
data and distribute among our team mates. For example our Gender DataFrame is shown below:

![](Images/genderDF.PNG)

The next section of work was graphing our DataFrame and beginning our Linear regression Model. The first 
graph is showing a trend of heart attack occurences by gender over the years. We the plot we show both Male
and Female, against the Year and Average Data Value. 

![](Images/genderplot.PNG)

Next we take this past data and now want to predict the future and where Heart Disease will go. Separately 
the Male and Female data is prepared for our prediction model. We call our Linear Regression Model .fit() 
the data then np.arange for the next ten years. Run this through .predict() for our future years. We plot our
prediction with Male and Female being graphed on the same plot. The plot is shown below.

![](Images/predicted.PNG)

The interesting part of the this model is that Heart Disease will decline in the next 10 years, with females
being predicted to have the lower drop in Heart Disease. While you are reading maybe let us know what you think
the reason is for the drop?

We used a RandomForest Model for the next section of code, our data is the index of the year and our labels 
is the gender. We run a Train_Test_Split for both Male and Female, using a random_state of 42 and a test_size
of 0.2. We call RandomForestRegressor with n_estimator = 100, and random_state = 42, .fit() the data, run a 
predict. We have a metric for our R^2 and mean squared error. Picture below.

![](Images/r2.PNG)

After seeing our metrics of the data, we use np.arange for the next ten years, run our predict models and then
plot our findings. 

![](Images/randompredict.PNG)
