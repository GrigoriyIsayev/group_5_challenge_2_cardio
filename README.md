
HEART DISEASE
-----------------------------------------------------------------------------------------------------
Did you know that someone dies from heart disease every 33 seconds?! Furthermore, 1 in 5 deaths is 
associated with with heart disease. Since 25% of deaths in the United States is related to heart disease,
we thought it would be appropriate research to conduct in order to investigate the likelihood is 
developing it. We believe that Americans have an obsession with tracking their health. For example, in 
2019 Apple sold 30.7 million iwatches which tracks health features such as heart rate. Additionally, 
the trend has been increasing with 40 million iwatches sold in 2021.
Due to those reasons, our project aims to predict heart disease on individuals based on their characteristics. 
Our Linear Regression Model shows the characteristics that can lead to higher chances of developing this disease.


Our project starts off with EDA. We imported our csv file, "Disease_Data.csv" from [DATA.GOV ](https://catalog.data.gov/dataset/rates-and-trends-in-hypertension-related-cardiovascular-disease-mortality-among-us-ad-2000-2fdf2)  
we broke this down to Race, Age, General and Overall. We conducted the following cleaning: 
1) Identified the N/As and removed then
2) dropped duplicated
3) dropped columns we were not using and only kept the columns below.
After cleaning the data, our final DataFrame is pictured below:

![](Images/dataframe.PNG)

After the DataFrame cleaning process, we moved on to breaking up the columns by our topics; Age, Gender, 
Race, and Overall. We decided to breakdown the DataDrame into topics due to two reasons: 
1) the original file was large in size 
2) divide the project across the team.
For example, our Gender DataFrame is shown below:

![](Images/genderDF.PNG)

The next section of work was graphing our DataFrame and beginning our Linear regression Model. The first 
graph is showing a trend of heart attack occurences by gender over the years. We the plot we show both Male
and Female, against the Year and Average Data Value. 

![](Images/genderplot.PNG)

The next section we will discuss the results across the topics staying of with Gender. The first figure is 
a line graph displaying our Linear regression Model results for Gender. The first figure, “Heart Attack 
Occurrences by Gender Over the Year” shows a trend of heart attack occurrences by gender over the years. The 
plot shows both males and females trended down from 2000-2010, however, the trend has changed. Since 2010, 
there has been an increase in occurrences for both genders. There is a difference though in the trend from 
2000-2010 and 2010 to now – in the first trend females had more occurrences than males.  Now, males have 
more occurrences than females.

In following figure “Heart Attack Occurrences by Gender”, we conducted a forecast using the past data to 
predict heart disease by gender. Linear Regression Model .fit() was used in the data then np.arange for the 
next ten years. This model was ran through .predict() for our future years. The plot is shown below.

![](Images/predicted.PNG)

We were surprised with the results since it was interesting to see the model expects Heart Disease to decline 
in the next 10 years, with females predicted to have lower Heart Disease in the upcoming years. While you are 
reading maybe let us know what you think the reason is for the drop?

Next, we used RandomForest Model. In our dataset, we placed the index as the year and our labels to be the gender.
We ran a Train_Test_Split for both males and females, using a random_state of 42 and a test_size of 0.2. We call 
RandomForestRegressor with n_estimator = 100, and random_state = 42,. fit() the data, ran a predict model. We have 
a metric for our R^2 and mean squared error. The figure below, “Heart Attack Occurrences by Gender and Predicted – Random Forest” 
shows the future years and what the model expects the heart disease rate to be by gender.

We continued our research by conducting age analysis using a Random Forest Regressor. First, we present the Random 
Forest figure displaying the results. Next, we include a figure titled "Major Cardiovascular Disease by Race 
(Actual and Predicted – Random Forest)," which shows the occurrences of heart disease by race and the model's 
predictions. Post-2020 predictions indicate varied trends for different racial groups, with some showing an increase 
and others showing stable or declining trends.

The current results indicate that Non-Hispanic Whites have the highest level of occurrences, and the model predicts 
this trend will remain stable. The second group with the highest rate is Non-Hispanic Blacks, while the Hispanic group 
has the lowest level of occurrences. Overall, the results suggest minimal changes in these trends in the coming years.

(raceactualpredicted)

Later in our research, we also continued our race analysis by implementing a Linear Regression Model. The figure below, 
“Major Cardiovascular Disease by Race (Actual and Predicted) displays major cardiovascular disease occurrences for various 
racial groups from 2021 to 2030. However, it predicts a different trend compared to the Random Forest Model. In the Linear 
Regression Model, the model expects Non-Hispanic White and Non-Hispanic Black occurrences to trend down.  

Potential Implications from the research results are health planning. For example, understanding these trends can help 
in resource allocation and targeted healthcare interventions for different racial groups.

(majorcardioactualpredict)

The final feature in our heart disease analysis was age. The results for this feature were particularly intriguing and 
unexpected. Using a Random Forest, model effectively captures the trends in major cardiovascular disease occurrences across 
different age groups from 2000 to 2020. Post-2020 predictions indicate varied trends for different age groups, with some showing 
an increase and others showing stable or declining trends.

Surprisingly, the age groups 75 and 65 showed similar occurrences to the 18-24 and 25-44 age groups. The age groups with the 
highest occurrences were 35-year-olds and those aged 45-65. Notably, these two groups have consistently had the highest rates 
since 2000. 

(randomforest3)

Again, the Linear Regression Model predicts slightly different results for age. Compared to the Random Forest Model, the linear regression model expects the age group 35 to have a decline. 
⦁	Predictions for the 18-24 age group show a stable trend.
⦁	Predictions for the 25-44 age group show a stable trend.
⦁	Predictions for the 45-64 age group show a declining trend.
⦁	Predictions for the 65+ age group show a stable or slightly increasing trend.
⦁	Predictions for the 75+ age group indicate a stable or slightly declining trend

(randomforest4)

![](Images/r2.PNG)

After seeing our metrics of the data, we use np.arange for the next ten years, we ran our predict models, and 
then plotted our findings below. 

![](Images/randompredict.PNG)

Here we see the predict model is showing us that things will plateau, and no change will happen for both Male 
Female. Interesting! 

Our next task was calculating the number of occurences by state per year. Here we count the number of occurences 
by the states and then we graph these values. We used a histogram to show our data.

![Alt text](Images/histo.PNG)

This project was a colaborration of our team to bring one of our members work to life. We all took different roles
and worked to build this Machine Learning Model to show case our findings. We hope you stay healthy and enjoy our
Machine Learning Algorithim. 
