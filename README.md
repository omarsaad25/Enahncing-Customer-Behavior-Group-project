# Enhancing-Customer-Behavior-for-Electronic-Sales
## Overview  
This project analyzes a dataset of sales transaction records from an electronics company over a one-year period (September 2023 to September 2024). The primary objective is to uncover key insights into customer behavior, product sales, and the impact of factors such as gender, loyalty programs, product ratings, and add-ons on overall sales performance.  

The dataset was sourced from Kaggle and includes detailed information about customer demographics, product types, and purchase behaviors.

## Objectives
* **Product Analysis by Gender**: Identify the most sold product by gender.
* **Top-Rated Products:** Calculate and analyze the highest-rated products using the IMDb rating formula.
* **Impact of Loyalty Membership:** Investigate how loyalty membership affects customer spending and the purchase of add-ons.
* **Purchasing Trends:** Analyze trends in purchasing behavior based on shipping type and purchase dates.
* **Revenue Analysis:** Determine which product types generate the most revenue and assess the contribution of add-ons to overall sales.
  
## Dataset Information
The dataset includes the following key features:  

* Customer ID: Unique identifier for each customer.
* Age: Customer age (numeric).
* Gender: Gender of the customer (Male or Female).
* Loyalty: Whether the customer is part of the loyalty program (Yes/No). This value may change over time, reflecting customers who cancel or join the program.
* Product Type: The type of electronic product sold (e.g., Smartphone, Laptop, Tablet).
* SKU: Unique code for each product.
* Rating: Customer rating of the product (1-5 stars).
* Order Status: Status of the order (Completed, Cancelled).
* Payment Method: Payment method used (e.g., Cash, Credit Card, PayPal).
* Total Price: Total value of the transaction.
* Unit Price: Price per unit of the product.
* Quantity: Number of units purchased.
* Purchase Date: Date of the purchase (format: YYYY-MM-DD).
* Shipping Type: Type of shipping selected (e.g., Standard, Overnight, Express).
* Add-ons Purchase: List of any additional items purchased, such as accessories or extended warranties.
* Add-on Total: Total price of add-ons purchased.
  
## Methodology
* **Data Cleaning**
  * Handling Missing Data:
  * No duplicated rows found.
  * Missing values in the "Gender" column were replaced with "Male" to avoid skewing the distribution.
  * Missing values in the "Add-ons Purchased" column were replaced with "N/A" if the "Add-on Total" value was zero.
    
* **Top-Rated Product Calculation**
The IMDb weighted rating formula was used to calculate top-rated products: ```WR= 
v+m
v
​
 ⋅R+ 
v+m
m
​
 ⋅C```

v: Number of votes for the product.

m: Minimum number of votes required to be listed in the chart (65th percentile).  

R: Average rating of the product.  

C: Mean rating across all products (calculated as 2.921).  

Products with more than 2005 votes (the minimum quantile threshold) were included in the final top-rated list.  


* **RFM Analysis**
  * Sorting: Transactions were sorted by purchase date to uncover patterns.
  * Boxplot Visualization: Used Seaborn to visualize distributions and detect outliers.
  * Correlation Analysis: Explored the relationships between features (e.g., Unit Price and Total Price correlation of 0.674).

## Visualization and Insights
We used a combination of **Python**, **R**, and **Tableau** for visualizations:  

* **Total Sales and YoY Growth:** Bar charts for total sales and year-on-year growth using Tableau.
* **Product Type Distribution:** Pie chart in Tableau to show sales contribution by product type.
* **Shipping Type by Quarter:** Bar chart in Tableau to compare sales trends by shipping type and purchase date.
* **Sales Trends by Date:** Line chart in Tableau to identify sales peaks and dips over time.

## Tools Used
* **Python:** Data cleaning, exploratory data analysis (EDA), and initial visualizations.
* **R:** Data cleaning, statistical analysis, and additional visualizations.
* **Tableau:** Creation of an interactive dashboard for deep data exploration and insights.

## Future Considerations
* **Loyalty Program Expansion:** Focus on enhancing customer retention through loyalty programs.
* **Customer Demographics:** Further analysis to explore deeper insights into purchasing behavior.
* **Targeted Marketing:** Use customer segmentation to launch targeted marketing campaigns.


## Results and Conclusion
Our analysis revealed key insights into customer behavior, product performance, and the impact of loyalty programs. The most significant findings included:  

* High-rated products had a strong influence on sales.
* Customers with loyalty memberships showed a higher propensity for add-on purchases.
* Shipping type and timing significantly influenced purchasing patterns.

