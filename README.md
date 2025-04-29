# Sales-Trend-Analysis-Using-Aggregations-in-MySQL

## Walmart Sales Data Analysis

### Overview
This project analyzes Walmart sales data to uncover insights on branch and product performance, customer behavior, and sales trends. The goal is to recommend strategies for optimizing sales and profitability.  

### Project Objectives
- Identify top-performing branches and products.
- Analyze sales patterns across time and product lines.
- Understand customer segmentation and behavior.
- Provide actionable recommendations for sales improvement.

### Dataset Description
The dataset includes 1,000 sales records across three Walmart branches (Mandalay, Yangon, Naypyitaw), featuring 17 columns:
| Column                  | Description                       |
| :---------------------- | :--------------------------------- |
| invoice_id              | Unique sales identifier           |
| branch                  | Branch code                       |
| city                    | Branch location                   |
| customer_type           | Customer segment                  |
| gender                  | Customer gender                   |
| product_line            | Product category                  |
| unit_price              | Price per unit                    |
| quantity                | Quantity purchased                |
| VAT                     | Value Added Tax (5%)              |
| total                   | Total bill (COGS + VAT)           |
| date                    | Date of transaction               |
| time                    | Time of transaction               |
| payment_method          | Payment method                    |
| cogs                    | Cost of goods sold                |
| gross_margin_percentage | Gross margin percentage           |
| gross_income            | Gross profit                      |
| rating                  | Customer rating                   |

### Areas of Analysis
1. **Product Analysis**  
   Analyze product lines to identify top performers and underperformers.
2. **Sales Analysis**  
   Examine sales trends and assess the effectiveness of different sales strategies.
3. **Customer Analysis**  
   Segment customers and evaluate their purchase behavior and profitability.

### Analysis Approach
1. **Data Cleaning:**  
   - Remove NULL values.
   - Create structured database tables with `NOT NULL` constraints.
2. **Feature Engineering:**  
   - `time_of_day`: Classify sales into Morning, Afternoon, Evening.
   - `day_name`: Extract weekday of transaction.
   - `month_name`: Extract month of transaction.
3. **Exploratory Data Analysis (EDA):**  
   - Analyze sales, product, and customer metrics.
4. **Insights and Recommendations:**  
   - Summarize findings for business improvement.
   - 
### Key Business Questions
- **General:**  
  - How many unique cities and branches are there?
- **Product Analysis:**  
  - Top-selling product lines?  
  - Highest revenue by city and product?  
  - VAT contribution by product lines?
- **Sales Analysis:**  
  - Sales patterns by time of day.
  - Customer types generating the most revenue.
- **Customer Analysis:**  
  - Customer and gender distribution.  
  - Trends in customer ratings by branch.

### Revenue and Profit Calculations
- **Cost of Goods Sold (COGS):**  
  \( \text{COGS} = \text{Unit Price} \times \text{Quantity} \)
- **Value Added Tax (VAT):**  
  \( \text{VAT} = 5\% \times \text{COGS} \)
- **Total Sale (Gross Sales):**  
  \( \text{Total} = \text{VAT} + \text{COGS} \)
- **Gross Profit (Gross Income):**  
  \( \text{Gross Income} = \text{Total Sales} - \text{COGS} \)
- **Gross Margin (%):**  
  \( \text{Gross Margin} = \frac{\text{Gross Income}}{\text{Total Revenue}} \)

### Example Calculation
- **Inputs:**  
  - Unit Price = \$45.79  
  - Quantity = 7  
- **Outputs:**   
  - COGS = 45.79 × 7 = \$320.53  
  - VAT = 5% × 320.53 = \$16.0265  
  - Total = 320.53 + 16.0265 = \$336.5565  
  - Gross Margin Percentage = (16.0265 ÷ 336.5565) ≈ 4.76%
