# Introduction
In this Visual Data Analysis, we examine a dataset from an anonymous company’s Facebook ad campaign.
The data file can be downloaded from [here](https://www.kaggle.com/loveall/clicks-conversion-tracking). 
The anonymous company is refered to as `company xyz` in this dataset. 
The file conversion_data.csv contains 1143 observations in 11 variables.

# Data Wrangling
Company xyz had 3 three different ad campaign ids which were in integer format.
I made a python function to change the integer values to 'campaign A', 'campaign B', and 'campaign C'.
I also made 4 new columns representing Click Through Rate, Cost Per Mille, Conversion Rate, and Cost Per Total Conversion.
There were several rows where Cost Per Total Conversion had infinite values, and I filtered them into a sub dataframe.

# Conclusions
* **For company xyz, there is a very high correlation between ad spend, clicks and impressions.**
* **However, there is a moderate correlation between ad spend and Approved Conversions (targeted people who actually buy products).**
* **Segmented by age, while people ages 30 - 34 are less likely to click an ad, once they click, they are more likely to buy products from company xyz.**
* **On the contrary, while people ages 45-49 are more likely to click an ad, once they click, they are less likely to buy products**
* **Segmented by Ad Campaign, campaign A had by far the lowest Cost Per Total Conversion and Cost Per Approved Conversion.**
* **Segmented by Gender, Females had much higher Cost Per Approved Conversion than Males.**
* **With the facts above, in this dataset, company xyz should target more potential customers with campaign A 
as it brought the most paying customers than the other two campaigns. Also, to get more customers with the least ad spend, 
they should target more males and people in the 30-34 age range.**
