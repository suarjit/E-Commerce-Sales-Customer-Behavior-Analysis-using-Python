# E-Commerce-Sales-Customer-Behavior-Analysis-using-Python
# E-Commerce Sales & Customer Behavior Analysis using Python

## 📌 Project Overview

This project focuses on analyzing e-commerce sales data and customer purchasing behavior using Python. It uses data cleaning, exploratory data analysis (EDA), statistical analysis, and visualization to understand product performance, country-wise revenue, sales trends, customer value, order values, cancellations, and changes in product demand.

The project aims to generate meaningful business insights that can support inventory management, customer retention, sales planning, and data-driven decision-making.

## 🎯 Project Objectives

- Identify products that generate the highest revenue.
- Analyze which countries contribute the most to total sales.
- Examine monthly and weekly sales trends.
- Identify products with the highest quantities sold.
- Calculate average and median order values.
- Identify high-value customers based on total spending.
- Detect unusual transactions and potential outliers.
- Calculate the percentage of cancelled invoices.
- Identify products with increasing or declining demand.
- Analyze the relationship between product price and quantity purchased.
- Generate business insights and recommendations from the analysis.

## 📂 Dataset

**Dataset file:** `Online Retail.csv`

The dataset contains e-commerce transaction records with information such as:

- `InvoiceNo` – Invoice or transaction number
- `StockCode` – Product identification code
- `Description` – Product description
- `Quantity` – Quantity purchased
- `InvoiceDate` – Date and time of the transaction
- `UnitPrice` – Price per unit
- `CustomerID` – Customer identification number
- `Country` – Country associated with the transaction

The code also creates additional columns, including:

- `IsCancelled` – Identifies invoices whose numbers begin with `C`
- `Revenue` – Calculated as quantity multiplied by unit price
- `Month` – Month associated with the transaction
- `Week` – Week associated with the transaction
- `Date` – Date associated with the transaction

## 🛠️ Tools and Technologies

- **Python** – Programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical calculations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Google Colab / Jupyter Notebook** – Development environment

## 🧹 Data Cleaning and Preparation

The project performs the following data preparation steps:

1. Loads the CSV dataset using Pandas.
2. Examines the dataset's shape, columns, first rows, and data types.
3. Checks for missing values and duplicate records.
4. Removes exact duplicate rows.
5. Standardizes text fields such as invoice numbers, stock codes, product descriptions, and country names.
6. Converts invoice dates to datetime format.
7. Converts quantity and unit price to numeric data types.
8. Identifies cancelled invoices using invoice numbers beginning with `C`.
9. Calculates line revenue using `Quantity × UnitPrice`.
10. Filters the sales data to exclude cancelled invoices, non-positive quantities, non-positive prices, invalid dates, and missing product descriptions.
11. Creates month, week, and date fields for time-based analysis.
12. Reports the number of valid sales rows and total valid sales revenue.

## 📊 Analysis Performed

### 1. Product Revenue Analysis
- Calculates total revenue, quantity sold, and number of unique invoices for each product.
- Identifies the top 10 products by revenue.
- Visualizes the highest-revenue products using a bar chart.

### 2. Country-Wise Sales Analysis
- Calculates total revenue, unique orders, and unique customers for each country.
- Identifies the top 10 countries by revenue.
- Visualizes country-wise revenue contributions.

### 3. Monthly and Weekly Sales Trends
- Calculates monthly revenue, quantity sold, and number of orders.
- Creates a line chart to analyze monthly revenue trends.
- Calculates weekly revenue and visualizes weekly sales patterns.
- Displays the first and last 10 weeks of sales data for inspection.

### 4. Product Quantity Analysis
- Calculates the total quantity sold and total revenue for each product.
- Identifies the top 10 products by quantity sold.
- Visualizes the products with the highest sales volumes.

### 5. Average Order Value Analysis
- Calculates order-level revenue by invoice number and country.
- Computes the average and median order values.
- Displays the distribution of order values using a histogram with a KDE curve.

### 6. Customer Value Analysis
- Groups sales by customer ID.
- Calculates total customer spending, number of orders, total quantity purchased, and last purchase date.
- Identifies the top 10 customers by total spending.
- Visualizes the highest-spending customers.

### 7. Outlier and Unusual Transaction Analysis
- Applies the Interquartile Range (IQR) method to identify potential outliers in:
  - Quantity
  - Unit price
  - Line revenue
  - Order value
- Calculates lower and upper outlier boundaries.
- Reports the number of potential outliers.
- Displays the 10 highest-revenue sales lines.
- Uses box plots to visualize the distributions of quantity, unit price, and revenue.

### 8. Invoice Cancellation Analysis
- Identifies unique invoices and their cancellation status.
- Calculates the number of cancelled invoices.
- Calculates the percentage of cancelled invoices.
- Visualizes cancelled and non-cancelled invoice counts using a bar chart.

### 9. Product Demand Analysis
- Calculates monthly quantities sold for each product.
- Divides the available months into two periods.
- Compares product quantities between the first and second periods.
- Calculates changes in quantity and percentage change where the first-period quantity is positive.
- Identifies products with the largest increases and decreases in demand.
- Visualizes products showing the largest demand changes.

### 10. Price and Quantity Relationship
- Calculates the Pearson correlation coefficient between unit price and quantity.
- Calculates the Spearman rank correlation coefficient.
- Creates a sample scatter plot to examine the relationship between unit price and quantity purchased.

### 11. Univariate and Bivariate Analysis
- Generates descriptive statistics for quantity, unit price, and revenue.
- Creates a country-by-month revenue pivot table.
- Calculates correlations among quantity, unit price, and revenue.
- Visualizes these relationships using a correlation heatmap.

### 12. Automatic Business Insights
The notebook automatically reports:

- The highest-revenue product.
- The highest-revenue country.
- Average order value.
- Percentage of cancelled invoices.
- Pearson correlation between price and quantity.

It also prints business recommendations related to product availability, marketing allocation, cancellation patterns, inventory planning, customer retention, and unusual transactions.

## 💡 Business Insights and Recommendations

The analysis can support the following business decisions:

- **Inventory management:** Monitor high-revenue and high-demand products to help maintain suitable stock levels.
- **Market expansion:** Compare country-wise revenue, order counts, and customer counts before allocating marketing budgets.
- **Sales planning:** Use monthly and weekly sales trends to support seasonal planning and inventory decisions.
- **Customer retention:** Use customer spending patterns to identify valuable customers and design appropriate retention campaigns.
- **Order management:** Investigate invoice cancellations to understand potential operational issues.
- **Demand forecasting:** Monitor products with increasing or declining sales quantities to support purchasing and stock planning.
- **Transaction monitoring:** Review unusually large quantities, prices, revenues, and order values.
- **Pricing analysis:** Use Pearson and Spearman correlations to explore the relationship between unit price and quantity purchased.

*Note: Statistical relationships and outliers should be interpreted carefully. Correlation does not prove causation, and an outlier is not automatically an error.*

## 📈 Expected Project Outcomes

After executing the notebook, the project produces:

- Cleaned sales data and calculated revenue.
- Top 10 products by revenue and quantity sold.
- Top 10 countries by revenue.
- Monthly and weekly sales trend charts.
- Average and median order values.
- Top 10 customers by total spending.
- An IQR-based outlier summary and high-revenue transaction list.
- Invoice cancellation counts and percentage.
- Products with the largest increases and decreases in demand.
- Pearson and Spearman correlation results.
- A correlation heatmap and business recommendations.

## 🚀 How to Run the Project

1. Clone or download this GitHub repository.
2. Download `Online Retail.csv` and place it in the same directory as the notebook.
3. Open `E-Commerce Sales & Customer Behavior Analysis using Python.ipynb` in Google Colab or Jupyter Notebook.
4. Install the required libraries if they are not already installed:

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

5. Make sure the CSV filename and file path match the code.
6. Run the notebook cells in order.
7. Review the generated tables, charts, statistical results, and business recommendations.

## ⚠️ Limitations

- The analysis depends on the quality and completeness of the available transaction data.
- Sales analysis excludes cancellations, non-positive quantities or prices, invalid dates, and rows without product descriptions.
- Customer-level analysis excludes records with missing customer IDs.
- Product demand comparisons depend on the months available in the dataset.
- Correlation does not establish a causal relationship between price and quantity.
- Potential outliers require further investigation before being classified as errors or unusual business events.
- Business recommendations should be evaluated alongside other operational and market information.

## 🏁 Conclusion

The **E-Commerce Sales & Customer Behavior Analysis using Python** project demonstrates how Python libraries can be used to transform raw transaction data into useful sales and customer insights. Through data cleaning, revenue calculations, trend analysis, customer segmentation by spending, cancellation analysis, demand comparison, correlation analysis, and visualization, the project provides a foundation for better inventory management, sales planning, and customer relationship strategies.

