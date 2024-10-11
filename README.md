# Happy Deliveries - Data Analysis Project

## Project Overview

Welcome to the **Happy Deliveries** data analysis project! This project involves analyzing data from a food delivery business operating in Ireland. The aim is to provide valuable insights from their sales and customer data, using data-driven decisions to help Happy Deliveries stay competitive in the food delivery market.

This project explores sales trends, customer demographics, and restaurant performance using datasets from 2021 and 2022. The analysis focuses on answering key business questions provided by Happy Deliveries and provides actionable insights.

## Data Sources

The project uses two datasets provided by the company:

- **Orders Dataset (`hd_orders.csv`)**: Contains details of orders placed through Happy Deliveries, including:
  - `order_id`: Unique ID of each order.
  - `order_timestamp`: Timestamp when the customer placed the order.
  - `delivered_timestamp`: Timestamp when the order was delivered.
  - `driver_id`: ID of the delivery driver.
  - `restaurant_id`: ID of the restaurant.
  - `cust_id`: ID of the customer who placed the order.
  - `delivery_region`: County in Ireland where the order was delivered.
  - `discount_applied`: True/False whether a discount was applied.
  - `discount_code`: Discount code used, if applicable.
  - `order_total`: Cost of the order before discounts, in euros (€).
  - `discount_pc`: Percentage discount applied to the order.
  - `status`: Status of the order (e.g., COMPLETED or CANCELLED).

- **Customers Dataset (`hd_customers.xlsx`)**: Contains details of loyalty card customers, including:
  - `id`: Unique ID of the customer.
  - `first_name`: First name of the customer.
  - `last_name`: Last name of the customer.
  - `age`: Age of the customer.
  - `city`: City in Ireland where the customer is based.
  - `email`: Customer's email address.

## Key Business Questions

This project answers the following key business questions:

1. How do the monthly sales in 2021 compare to 2022, and has sales growth been observed?
2. What is the age distribution of loyalty card customers?
3. Is there a relationship between the amount spent by a loyalty cardholder and their age?
4. Is there a relationship between the amount of a payment, the age of a person, and whether they used discount codes?
5. How do the sales in 2022 compare across different regions in Ireland?
6. Who are the top 10 highest spending customers in 2022? (For marketing rewards)
7. What are the top 3 restaurants in terms of sales for 2022?
8. Which customers made only one purchase in 2021 and are non-returning?
9. How successful was the `BLACKFRIDAY22` discount code compared to the `BLACKFRIDAY21`?
10. What locations had the lowest cumulative sales in 2022, and should marketing efforts focus on these regions?

## Data Cleaning

### Cleaning Steps:

1. **Orders Dataset**:
   - Removed orders with a status of "CANCELLED".
   - Filled missing values in the `discount_code` and `discount_pc` columns with "No Discount" and `0`, respectively.
   - Converted `order_timestamp` and `delivered_timestamp` to `datetime` format for accurate time-based analysis.

2. **Customers Dataset**:
   - Removed entries where customer age was greater than 100, as these were unrealistic values.

3. **Handling Missing Data**:
   - Missing values in the `delivered_timestamp` column were retained for further investigation but marked as potentially incomplete data.

## Data Analysis

The data analysis includes the following steps:

### 1. Monthly Sales Comparison (2021 vs. 2022)
   - Analyzed and visualized monthly sales totals to determine if the company's sales have grown over time.

### 2. Age Distribution of Loyalty Card Customers
   - Visualized the age distribution of loyalty card customers to understand the demographic profile of Happy Deliveries customers.

### 3. Relationship Between Spending and Age
   - Explored the correlation between customer age and total spending, identifying potential age groups that contribute significantly to revenue.

### 4. Impact of Discounts on Spending
   - Investigated how discount codes affect customer spending patterns, with a focus on the relationship between customer age and payment amounts.

### 5. Sales by Region (2022)
   - Compared the sales performance across various regions in Ireland in 2022 to identify high-performing and underperforming regions.

### 6. Top 10 Highest Spending Customers (2022)
   - Identified the top 10 customers based on total spending in 2022, along with their contact information, for a potential marketing campaign.

### 7. Top 3 Restaurants (2022)
   - Identified the top 3 restaurants based on total sales in 2022 to help allocate resources more effectively during peak periods.

### 8. Non-returning Customers (2021)
   - Identified customers who only made one purchase in 2021 and have not returned, providing insights for a churn reduction campaign.

### 9. Success of `BLACKFRIDAY22` vs. `BLACKFRIDAY21`
   - Compared the success of the two Black Friday discount codes in terms of total sales.

### 10. Regions with Lowest Sales (2022)
   - Identified regions with the lowest sales in 2022 and considered external factors such as population size that might influence these results.

## Project Structure

```plaintext
happy_deliveries_project/
│
├── data/                        # Folder for datasets
│   ├── customers_cleaned.csv     # Cleaned Customers dataset
│   ├── hd_customers.xlsx         # Original Customers dataset
│   ├── hd_orders.csv             # Original Orders dataset
│   └── orders_cleaned.csv        # Cleaned Orders dataset
│
├── notebooks/                    # Folder for Jupyter notebooks
│   ├── new_happy_case_data_cleaning.ipynb    # Data cleaning notebook
│   └── Happy_case_Exploratory_Data_Analysis.ipynb   # EDA notebook
│
├── .gitignore                    # Git ignore file to exclude unnecessary files from version control
│
├── README.md                     # Project overview and description
│
└── requirements.txt              # Python package dependencies



