Christmas Sales and Trends Dashboard
Dashboard Link: Christmas Sales Analysis Dashboard
Problem Statement
This dashboard provides retailers with insights into customer behavior during the Christmas season. By analyzing sales data, retailers can identify top-selling products, understand customer demographics, and evaluate the effectiveness of marketing strategies. The goal is to enhance decision-making for future holiday seasons by pinpointing successful areas and identifying opportunities for improvement.
Steps Followed
1.	Data Loading:
o	Imported the sales dataset (EXCEL file) into Power BI Desktop.
2.	Data Cleaning and Preparation:
o	Opened Power Query Editor to assess data quality.
o	Enabled "Column Distribution," "Column Quality," and "Column Profile" under the View tab.
o	Performed column profiling based on the entire dataset.
o	Addressed missing or erroneous values as necessary.
o	Replacing values with false and true with not and yes.
3.	Data Modeling:
o	Created relationships between tables, such as linking Location data with CSE table.
o	Established a Date table to facilitate time-based analyses.
4.	Calculated Columns and Measures:
Calculated  measure
code
Total Customers = DISTINCTCOUNT('CST'[Age])
Total Customers: Computed the distinct count of customers



Calculated measure
code
Total Transactions = COUNTROWS('CST')
Total Transactions: Determined the number of transactions

Calculated measure
Code
Total Sales = SUM('CST'[TotalPrice])

Calculated table
Code
= Table.Sort(#"Removed Duplicates",{{"Location", Order.Ascending}})

5.	Visualization Design:
o	Slicers: Added slicers for fields like "Event", "Wheather," and "Return flag" to enable dynamic filtering.
o	KPI Cards: Displayed key metrics such as Total Sales, Total Transaction,average of Delivery time,sum of Amount to pay.
o	Bar Charts: Illustrated sum of Delivery Time by Location.
o	Pie Charts: Depicted sum of Age by Payment Type and Total transaction by PaymentType.
o	Column Chart: Track sum of Unit price by event and Total Transaction by customer satisfaction.
6.	Interactivity and Drill-Through:
o	Enabled drill-through features to allow users to explore detailed data, such as viewing individual transactions for a specific product.
o	Configured interactions between visuals to ensure cohesive data exploration.

7.	Theming and Formatting:
o	Applied a festive theme with appropriate color schemes to enhance visual appeal.
o	Ensured consistent formatting for readability, including font sizes and number formats.
8.	Publishing:
o	Published the report to Power BI Service for accessibility and sharing with stakeholders.
Insights
1. Key Metrics:
•	Total Transactions: 10K
•	Total Sales: ₹1.65M
•	Average Delivery Time: 3.00
•	Sum of Amount to Pay: ₹1.58M
•	Insight: High sales and transactions indicate a successful event, while the average delivery time highlights logistics efficiency.
 2.  Sales Performance Over Time:
•	Total Sales by Year: Sales are consistent, around ₹200K annually from 2018 to 2023.
•	Insight: Stable sales over the years suggest reliable performance and potential growth opportunities.
3. Payment Type Preferences:
•	Total Transactions by Payment Type:
o	Debit Card: 2K (20%)
o	Cash: 3K (30%)
o	Credit Card: 2K (20%)
o	Online Payment: 3K (30%)
•	Insight: Cash and online payments are the most popular methods, indicating a balanced preference between traditional and digital payment options.
4. Customer Demographics by Payment Type:
•	Sum of Age by Payment Type:
o	Debit Card: 105K
o	Online Payment: 112K
o	Credit Card: 110K
o	Cash: 111K
•	Insight: The age distribution is fairly balanced across all payment types, suggesting diverse customer demographics.
5. Event Sales Performance:
•	Sum of Unit Price by Event:
o	Black Friday: ₹0.23M
o	Christmas Market: ₹0.16M
o	None: ₹0.16M
•	Insight: Black Friday significantly boosts sales, highlighting its importance in driving revenue.
6. Overall Customer Satisfaction:
•	Customer Satisfaction: 1.65M (gauge shows room for improvement)
•	Insight: The overall satisfaction score indicates a generally positive customer experience but suggests opportunities for enhancing satisfaction.
7.	Total Sales by Event:
Black Friday: ₹695.45K
Christmas Market: ₹483.57K
None: ₹475.23K
Insight: Black Friday has the highest sales, indicating it is a critical event for boosting sales.
8.	Customer Satisfaction by Transaction:
Range: Scores 1 to 5
Insight: All customer satisfaction scores have around 2,000 to 2,100 transactions, showing a relatively consistent distribution of customer satisfaction.
9.	Sum of Customer Satisfaction by Gender:
Female: 33.2%
Male: 33.76%
Other: 33.04%
Insight: Customer satisfaction is quite evenly distributed across genders.
10.	Overall Customer Satisfaction:
Total: 1.65M
Insight: Gauge shows the satisfaction range between 0.00M to 3.31M, indicating room for improvement.
11.	Sum of Delivery Time by Location:
City 17: 882
City 18: 863
City 5: 861
Insight: City 17 has the longest delivery times, suggesting a potential issue with logistics in this location.
12.	Total Sales by Category:
Toys: ₹340K
Electronics: ₹337K
Food: ₹333K
Decorations: ₹324K
Clothing: ₹321K
Insight: Toys and electronics are the top-performing categories.
13.	Sales by Category and Event:
Insight: Toys, Electronics, and Food categories perform well during Black Friday, indicating a strong influence of this event on these categories.
14.	Filters:
Event: Black Friday, Christmas Market, None
Weather: Rainy, Snowy, Sunny
Return Flag: Not, Yes
Insight: Allows for customized views to analyze specific scenarios and conditions.

