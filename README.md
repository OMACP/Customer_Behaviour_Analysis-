Customer Shopping Behavior Analysis

An end-to-end retail analytics project analyzing customer shopping behavior using Python, SQL Server, and Power BI — covering data cleaning, feature engineering, SQL-based business analysis, and an interactive 5-page dashboard.

🛠️ Tools Used

Python (pandas) · SQL Server · SQLAlchemy · Power BI · DAX · Power Query


📊 Dashboard Preview

The Power BI dashboard includes 5 pages: Overview, Demographics, Products & Category, Purchase Behavior, and Discounts & Promotions.

Key metrics: 3,900 customers | $233.08K total revenue | $59.76 avg purchase | 3.75 avg rating | 97.87% repeat customer rate


🗂️ Dataset


3,900 rows × 18 columns
Fields: Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount, Location, Size, Color, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Payment Method, Frequency of Purchases


🧹 Data Cleaning & Feature Engineering (Python / pandas)


Imputed missing Review Rating values using category-wise median
Standardized column names (lowercase, snake_case) and renamed ambiguous fields
Engineered age_group (Young Adult / Adult / Middle-aged / Senior) via quartile binning on age
Engineered purchase_frequency_days by mapping purchase frequency labels (Weekly, Monthly, Quarterly, etc.) to numeric day intervals
Dropped redundant promo_code_used column
Loaded the cleaned DataFrame into SQL Server using SQLAlchemy + pyodbc


🗃️ SQL Analysis

10 business questions answered with SQL, including:


Total revenue by gender
Customers who spent above average despite receiving a discount
Top 5 products by average review rating
Standard vs Express shipping — average purchase amount comparison
Subscribed vs non-subscribed customer spending comparison
Top 5 products by discount usage rate
Customer segmentation: New / Returning / Loyal (based on previous purchases)
Top 3 products per category (using ROW_NUMBER() window function)
Relationship between repeat purchases and subscription status
Revenue contribution by age group


Full queries: customer_project_sql.sql


📈 Power BI Dashboard



<img width="1236" height="738" alt="Screenshot 2026-07-16 135310" src="https://github.com/user-attachments/assets/4c397be3-2089-48f3-ae26-1c69d61ce219" />
<img width="1302" height="736" alt="Screenshot 2026-07-16 135347" src="https://github.com/user-attachments/assets/b77488bc-a012-4d4a-b449-ebdbc9524444" />
<img width="1301" height="732" alt="Screenshot 2026-07-16 135330" src="https://github.com/user-attachments/assets/6ebd34db-1ebe-4012-be7b-ac99f1c40a42" />
<img width="1101" height="731" alt="Screenshot 2026-07-16 135425" src="https://github.com/user-attachments/assets/5a820c45-be96-4f3e-9f55-2bf6d9726e0e" />
<img width="1220" height="737" alt="Screenshot 2026-07-16 135405" src="https://github.com/user-attachments/assets/d52a9abc-bbd1-4160-ac6d-59e454391b25" />




