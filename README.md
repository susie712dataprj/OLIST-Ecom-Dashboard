# OLIST Ecom Dashboard
# Introduction
Applying the Brazilian E-Commerce Public Dataset by Olist found on Kaggle, I built a dashboard monitoring all the commercial activities at Kaggle such as: order trends, customer behavior, and sales performance. The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers
# Overview
I use 2 software:
Google Sheets: This is just for connecting data through Power Query.
* We used a translation function to translate the customer’s review.
* Add brazil_states table to get more external data.
* Add some sub tables like RFM_segments in PBI.
Please visit the [[sheet](https://docs.google.com/spreadsheets/d/1uwOaJoMisEK2uD89ya0E4h-EXW6V5mxI8ap5k1LNtdg/edit?usp=sharing)] here

Power BI: Main working file, all the data cleaning process to visualization is done in Power BI.
## Data Schema
![image](https://github.com/user-attachments/assets/7a9cd7b7-0ad1-443d-8cd0-be09957356a5)
All the relationship are then built in Data Model in PBI
## Dataset Information
Visit [[Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)] for a detailed description of variables.

# Visualization
Download PBI file [[here](https://github.com/susie712dataprj/OLIST-Ecom-Dashboard/blob/main/OLIST%20Ecom%20Dashboard.pbix)] for better interactive dashboard
## Overall Performance
<img width="1418" alt="Ảnh màn hình 2024-08-28 lúc 16 24 49" src="https://github.com/user-attachments/assets/0e299c58-526e-42a6-8b32-f4923c6c7d29">

* Beside general metrics, OLIST get an extremly high completion rate with 96.85%, means that almost all the orders are succesfully delivered.
* Almost every categories experienced GOOD growth rate, especially for BOOKS with 44.32% increasing.
* LEISURE items demonstrate significant down trend with 17.55% decreasing.
* São Paulo generate the most GMV with 627,772 R$, three times higher than the second highest country which is Rio de Janeiro.

## Sales by Region
<img width="1181" alt="Ảnh màn hình 2024-08-29 lúc 08 37 50" src="https://github.com/user-attachments/assets/c50ae82d-406b-45bc-a44a-220a9405aea6">

* Correlation Analysis between Revenue & GDP and Revenue & Population -> All show strong positive relationship -> If the Population or GDP
increases, the Revenue also increases (vice versa)
* São Paulo's sales accounts for half of the sales among 27 states with 42.66% since it is the most populous state in Brazil largest GDP
* In terms of Region, SOUTHEST is dominant of sales concentration.
  
## Product/Category Performance
<img width="1418" alt="Ảnh màn hình 2024-08-29 lúc 08 41 58" src="https://github.com/user-attachments/assets/2f29cf9b-6574-43c2-a985-ca96f93b6a7d">

* Electronics leads with 22.59% of total sales, followed by Leisure at 19.78%, and Furniture & Decoration at 19.31%.
* Bed, Bath & Table items top the sales volume with 1,162 units sold, followed by Health & Beauty and Sports & Leisure. Items like Watches & Gifts and Telephony have lower quantities sold, possibly indicating niche markets or lower purchase frequency.
* In terms of comparison between AOV and Revenue:
  * **Low Revenue, High AOV Categories:** Fashion, Home Construction, Office & Stationery: These may have smaller customer bases but higher willingness to spend per transaction.
  * **High Revenue, Low AOV Categories:** Furniture & Decoration, Health & Beauty: These are likely driven by lower-priced items with a broad customer base, resulting in higher sales volumes but lower AOV

## Customer Behaviour
<img width="1420" alt="Ảnh màn hình 2024-08-29 lúc 08 50 14" src="https://github.com/user-attachments/assets/e96684db-1561-409a-a059-21a0555d8d67">

* RFM Segmentation:
  * Promising: The largest segment, making up 35.88% of customers. These are recent purchasers who haven't spent much, indicating potential for future engagement.
  * Cannot Lose Them: This critical segment represents 19.99% of customers who are valuable but may be at risk of leaving. Strategies should focus on retaining them.
  * However, the current customer base at OLIST are most one-time buyer -> Lacking Loyalty segments.
* Peak Times for Shopping on Olist:
  * High traffic on WORKDAYS FROM AFTERNOON
  * Midnight to Morning (0-11) shows consistently low order activity across all days, suggesting that Olist customers are not familiar with or interested in midnight shopping.
* The Average Monetary Value per customer is 155.48 R$, which is a useful benchmark for evaluating the success of customer retention and upselling strategies.
* São Paulo dominates with 4,272 customers, followed by Rio de Janeiro with 1,338 customers.

## Customer Review Analysis 
<img width="1410" alt="Ảnh màn hình 2024-08-29 lúc 09 01 58" src="https://github.com/user-attachments/assets/16ca8cb5-d2ce-43ed-979d-b971581f0e0f">

* Customer satisfaction is generally high. The average review score is 4.00 out of 5, and the majority of reviews are positive. The highest rating category is Books.
* Do Delivery affect Rating Score?
  * If orders were delivered LATE => high chances getting lower review score (10% distribution decrease on score 5 compare to On-time)
  * If the orders were LATE delivered, OLIST's need to ensure that it had to be no later than 10 days.
  * The orders were delivered after 10 days of limit shipping days => HIGHER chance to receive below 3 rating

