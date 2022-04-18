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

<img width="521" alt="mean_ctr_age_gender" src="https://user-images.githubusercontent.com/90280839/163756073-b116ef6b-1666-403e-a0ac-a55dc3071673.png">

**Above, the CTR is the highest amongst the 45-49 age group. Females in this dataset have a higher CTR than males. Like the heatmap, it shows that high CPM costs are correlated with a higher Click Through Rate for Company xyz's ad campaigns.**

<img width="533" alt="CTR_campaign_id" src="https://user-images.githubusercontent.com/90280839/163756121-5479f5c3-4ae1-4972-9821-dde122b9e1c3.png">

**Above, Campaign A has the highest Click Through Rate.**

<img width="528" alt="CPTC_campaign_id_gender" src="https://user-images.githubusercontent.com/90280839/163756159-f1ac3d53-734f-4ca2-ad03-53c65e8e13aa.png">

**Above, the Cost Per Total Conversion is lowest for campaign A. The Cost Per Total Conversion is highest for campaign A. The CPTC is higher for females than males. Therefore, it is more expensive to get females interested in company xyz's product.**

<img width="514" alt="ad_spend_approved_conversion_corr" src="https://user-images.githubusercontent.com/90280839/163756188-5ce48b0a-f642-4d57-abd7-7462173c2c40.png">

**Above, there is a moderate correlation (0.59) between Ad Spend and Approved Conversion for company xyz.**

<img width="523" alt="cos_per_approved_conversion" src="https://user-images.githubusercontent.com/90280839/163756225-d65e3fc9-42ad-4cd9-b6f8-7aaced5a16ef.png">

**Above, Campaign A had the lowest Cost Per Approved Conversion. Campaign C had the highest Cost Per Approved Conversion. Campaign A was the most effective at making consumers buy with the lowest cost.**

<img width="507" alt="CPA_by_gender" src="https://user-images.githubusercontent.com/90280839/163756271-65ad567e-8497-4c14-9e63-cf800f7ac929.png">

**Cost Per Approved Conversions are much higher amongst Females than Males.**

<img width="507" alt="CPA_by_age" src="https://user-images.githubusercontent.com/90280839/163756309-00efa59d-ace2-46b4-aa64-cb4b547d1765.png">

**Cost Per Approved Conversions is highest amongst ages 45 - 49. Cost Per Approved Conversions is lowest amongst ages 30-34.**

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
