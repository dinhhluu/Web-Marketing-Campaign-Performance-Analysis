# Web Marketing Campaign Performance Analysis

## Project Overview
This project analyzes web marketing campaign performance using session-level data from a simulated e-commerce website. The study focuses on understanding user behavior, conversion patterns, and revenue generation across different traffic sources, marketing campaigns, user types, and device categories.

The analysis combines exploratory data analysis (EDA), statistical testing, correlation analysis, and regression modeling to evaluate the effectiveness of marketing channels and user engagement metrics.

## Research Objectives
This project aims to analyze web marketing campaign performance using session-level data in order to understand user behavior, conversion patterns, and revenue generation. 
The main objectives of the study are: 
- To explore user behavior characteristics such as session duration, page views, and engagement. To compare conversion performance across different user segments (new vs. returning users). 
- To examine how conversion rates and revenue vary by traffic source, medium, campaign, and device category. 
- To investigate the relationship between behavioral metrics, conversions, and revenue using correlation analysis. 
- To evaluate the effectiveness of predictive models (logistic regression for conversion and linear regression for revenue) in explaining marketing outcomes.

## Data Overview
In the context of increasing competition in e-commerce, understanding user behavior and the effectiveness of online marketing campaigns plays a crucial role in optimizing conversion rates and revenue. The dataset used in this thesis records user interactions with web marketing campaigns of a simulated e-commerce website over the period from June 1, 2023 to June 30, 2023.

### Data Source
The dataset is stored in a CSV file named web_marketing_data.csv. Each observation represents a single user session recorded between June 1, 2023 and June 30, 2023.
 
### Data Desrciption
The dataset consists of 10,000 observations and includes multiple groups of variables that comprehensively reflect key aspects of user behavior and marketing campaign performance. Specifically, the variables cover session time information, in-session behavioral characteristics, marketing sources and channels, device types, geographic locations, as well as conversion outcomes and revenue. As a result, the dataset enables in-depth analysis of user behavior, evaluation of marketing campaign effectiveness, and the development of predictive models for user conversion.

Date: The date of the user session (MM/DD/YYYY).

User_ID: A unique identifier for each user.

Session_Duration: The duration of the user’s session in seconds.

Page_Views: The number of pages viewed by the user during the session.

Source: The origin of the user’s traffic (e.g., Referral, Social, Direct, Organic).

Medium: The marketing medium used (e.g., Direct, Social Media, Organic Search, Referral). Note: “Referral” can appear in both Source and Medium, indicating different types of referrals. Source “Referral” implies the user came from another website, while Medium “Referral” suggests a referral link or campaign.

Campaign: The specific marketing campaign associated with the session (e.g., Spring Promo, Summer Sale, Winter Campaign). Blank values indicate sessions not directly linked to a specific campaign.

Device_Category: The type of device used by the user (e.g., Desktop, Mobile, Tablet).
Country: The user’s geographic location.

New_User: A binary indicator (1 for new user, 0 for returning user).

Conversions: The number of conversions attributed to the user during the session.

Revenue: The revenue generated from the user during the session (in USD).

## Data Preprocessing & Feature Engineering
Missing values were handled appropriately (e.g., missing campaign values grouped as Others).
Data types were standardized, and date fields were converted to datetime format.
Outliers were examined using the IQR method, with no abnormal values detected.
Additional features were created to support analysis:

- Engagement = Page Views / Session Duration

- Conversion Rate = Conversions / Page Views

- Revenue per Conversion

- User_Type (New vs. Returning)

## Exploratory Data Analysis (EDA)
The exploratory analysis examines:

- Distribution of key behavioral variables

- Conversion rate differences across:

	- 	User type

	- 	Traffic source and medium

	- 	Marketing campaign

	- 	Device category

- Weekly trends in conversion rate and total revenue
Visualizations are used extensively to highlight patterns and trends.

## Correlation Analysis
Both Pearson and Spearman correlation analyses were conducted to identify linear and non-linear relationships among key variables.
Key findings include:

- A very strong relationship between Conversions and Revenue

- Moderate associations between Page Views and Engagement

- Minimal correlation between most session-level behavior metrics and revenue

## Statistical Testing
Non-parametric Mann–Whitney U tests were applied to compare behavioral differences between new and returning users.
The results indicate no statistically significant differences at the 5% significance level.

## Regression Analysis
### Linear Regression (Revenue)
A multiple linear regression model was used to explain revenue variation.
The model shows very limited explanatory power (R² ≈ 0.001), suggesting that session-level behavioral and campaign variables alone are insufficient to explain revenue outcomes.

### Logistic Regression (Conversion)
A logistic regression model was applied to predict conversion occurrence.
The model is not statistically significant overall, and none of the explanatory variables show significant effects at the 5% level.
Although test accuracy is relatively high, this performance is largely driven by class imbalance rather than strong predictive relationships.

## Key Insights

- Conversion rates are relatively stable across user segments, traffic channels, campaigns, and devices.

- Revenue variation is driven primarily by conversion volume rather than individual session behavior.

- Returning users do not generate higher revenue per conversion compared to new users, indicating untapped monetization potential.

- Session-level engagement metrics alone are weak predictors of conversion and revenue.

## Discussion and Limitations 
Although extensive exploratory data analysis and statistical modeling were conducted, several limitations should be acknowledged: 
- Most observed differences in conversion rates across user types, traffic sources, campaigns, and devices are relatively small and often not statistically significant, indicating limited explanatory power at the session level. 
- The logistic regression model for conversion did not achieve overall statistical significance, suggesting that key drivers of conversion may not be fully captured by the available variables. 
- The linear regression model for revenue shows a very low R-squared value, implying that revenue variation is largely driven by factors beyond session behavior, such as pricing strategies, product mix, or external influences. 
- Engagement is a derived metric based on page views and session duration, which may introduce mechanical correlations rather than true behavioral causality. 
- The analysis is limited to a short time window and does not account for seasonality, long-term user behavior, or repeated user journeys across sessions.

## Final Conclusion
Overall, the analysis indicates that conversion rates are relatively stable across different user segments, traffic channels, campaigns, and devices, while revenue exhibits greater variability driven primarily by the number of conversions rather than session-level engagement metrics. Correlation analysis confirms that conversions are the strongest determinant of revenue, whereas individual behavioral metrics such as page views and session duration alone are weak predictors. 
The findings suggest that improving revenue performance may require strategies focused on increasing transaction value and conversion volume rather than solely optimizing on-site behavioral metrics. From a business perspective, the results highlight opportunities for better monetization strategies, especially for returning users, and the need for more granular data to build stronger predictive models.

## Notebook
Run the full analysis on Google Colab: https://colab.research.google.com/drive/1GaAsw57H5LAbCcfFu1p2zGFZ2erL6M2M?usp=sharing 
