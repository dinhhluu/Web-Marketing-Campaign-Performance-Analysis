# Web Marketing Campaign Performance Analysis
## Data Overview

In the context of increasing competition in e-commerce, understanding user behavior and the effectiveness of online marketing campaigns plays a crucial role in optimizing conversion rates and revenue. The dataset used in this thesis records user interactions with web marketing campaigns of a simulated e-commerce website over the period from June 1, 2023 to June 30, 2023.

### Data Source
The data is stored in a CSV file named web_marketing_data.csv, in which each observation represents a user session on the website.
 
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


Dựa trên tập dữ liệu này, bài luận tập trung phân tích hiệu quả của các kênh marketing và chiến dịch quảng cáo, cũng như hành vi người dùng trên các thiết bị khác nhau.
Trước khi tiến hành phân tích và xây dựng mô hình dự đoán, dữ liệu cần được kiểm tra và làm sạch nhằm đảm bảo tính nhất quán và độ tin cậy. Trong nghiên cứu này, Python được sử dụng để thực hiện các bước kiểm tra và làm sạch dữ liệu ban đầu do khả năng truy vấn hiệu quả và dễ tái lập trên tập dữ liệu lớn, đồng thời dùng để phân tích mối quan hệ giữa các biến và dự báo.


