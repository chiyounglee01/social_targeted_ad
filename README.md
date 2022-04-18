## Introduction
In this Visual Data Analysis, we examine a dataset from an anonymous company’s Facebook ad campaign.
The data file can be downloaded from [here](https://www.kaggle.com/loveall/clicks-conversion-tracking). 
The anonymous company is refered to as `company xyz` in this dataset. 
The file conversion_data.csv contains 1143 observations in 11 variables.

## Data Wrangling
Company xyz had 3 three different ad campaign ids which were in integer format.
I made a python function to change the integer values to 'campaign A', 'campaign B', and 'campaign C'.
I also made 4 new columns representing Click Through Rate, Cost Per Mille, Conversion Rate, and Cost Per Total Conversion.
There were several rows where Cost Per Total Conversion had infinite values, and I filtered them into a sub dataframe.

## Visual Data Exploration

<img width="548" alt="ad_id_count_age" src="https://user-images.githubusercontent.com/90280839/163755545-c72a9dcf-2e28-440a-ac8d-8d6d6171c785.png">

**Above, people age 30-34 had more ads targeted towards them than any other age group. People age 40-44 had the least amount of ads targeting towards them. Although a little more ads were targeted towards males, there isn't a huge difference in the amount of ads target towards males vs females.**

<img width="558" alt="ad_id_count_campaign_id" src="https://user-images.githubusercontent.com/90280839/163755619-43f0eb79-9df4-489d-97cc-252729a1f330.png">

**Above, of the 1143 Ad IDs in the df_c dataframe, half of them were part of campaign C. Less than 10 percent of the Ad IDs were part of campaign A. More males than females were targeted for campaign A and C, while more females than males were targeted for campaign B.**

<img width="606" alt="approved_correlation" src="https://user-images.githubusercontent.com/90280839/163755848-6553790f-8873-42ba-860b-2e8337b9bf8f.png">

**Above, there is a very high correlation (0.99) between ad spend by company xyz and clicks. There is also a very high correlation (0.97) between ad spend and impressions. There is a lower correlation between ad spend and Total Conversions (0.81). There is a low correlation between ad spend and Approved Conversions. Company xyz's social ads are good at getting impressions and clicks, but they are not as effective in making consumers actually buy products.**

<img width="482" alt="CTR_correlation" src="https://user-images.githubusercontent.com/90280839/163755873-e80e192f-324e-42d6-a503-796d7b068329.png">

**Above, there is a high correlation between Cost Per Mille(Thousand) and Click Through Rate (0.96). But in general there is a low correlation between Click Through Rate, Cost Per Mille(Thousand), Conversion Rate and Cost Per Total Conversion.**

<img width="532" alt="average_cpm_age_gender" src="https://user-images.githubusercontent.com/90280839/163755911-75179cfd-96e7-4397-841b-d76e8bf6b377.png">

**Above, the CPM is highest amongst the 45-49 age group. Females in this dataset have a higher CPM than males.**



## Conclusions
* **For company xyz, there is a very high correlation between ad spend, clicks and impressions.**
* **However, there is a moderate correlation between ad spend and Approved Conversions (targeted people who actually buy products).**
* **Segmented by age, while people ages 30 - 34 are less likely to click an ad, once they click, they are more likely to buy products from company xyz.**
* **On the contrary, while people ages 45-49 are more likely to click an ad, once they click, they are less likely to buy products**
* **Segmented by Ad Campaign, campaign A had by far the lowest Cost Per Total Conversion and Cost Per Approved Conversion.**
* **Segmented by Gender, Females had much higher Cost Per Approved Conversion than Males.**
* **With the facts above, in this dataset, company xyz should target more potential customers with campaign A 
as it brought the most paying customers than the other two campaigns. Also, to get more customers with the least ad spend, 
they should target more males and people in the 30-34 age range.**
