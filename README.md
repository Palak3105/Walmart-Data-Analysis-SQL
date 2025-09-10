# Walmart-Sales-Data-Analysis-SQL  

## 📌 About  
This project aims to explore the Walmart Sales data to understand:  
- Top performing branches and products  
- Sales trend of different products  
- Customer behaviour  

The aim is to study how sales strategies can be improved and optimized.  
The dataset was obtained from the **Kaggle Walmart Sales Forecasting Competition**.  

> "In this recruiting competition, job-seekers are provided with historical sales data for 45 Walmart stores located in different regions. Each store contains many departments, and participants must project the sales for each department in each store. To add to the challenge, selected holiday markdown events are included in the dataset. These markdowns are known to affect sales, but it is challenging to predict which departments are affected and the extent of the impact." — *Source: Kaggle*  

---

## 🎯 Purpose of the Project  
The major aim of this project is to gain insight into the sales data of Walmart to understand the different factors that affect sales of the different branches.  

---

## 📊 About the Data  
The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition.  
This dataset contains sales transactions from three different branches of Walmart, respectively located in **Mandalay, Yangon, and Naypyitaw**.  

- **17 columns**  
- **1000 rows**  

| Column | Description | Data Type |
|--------|-------------|-----------|
| invoice_id | Invoice of the sales made | VARCHAR(30) |
| branch | Branch at which sales were made | VARCHAR(5) |
| city | The location of the branch | VARCHAR(30) |
| customer_type | The type of the customer | VARCHAR(30) |
| gender | Gender of the customer making purchase | VARCHAR(10) |
| product_line | Product line of the product sold | VARCHAR(100) |
| unit_price | The price of each product | DECIMAL(10,2) |
| quantity | The amount of the product sold | INT |
| VAT | The amount of tax on the purchase | FLOAT(6,4) |
| total | The total cost of the purchase | DECIMAL(10,2) |
| date | The date on which the purchase was made | DATE |
| time | The time at which the purchase was made | TIMESTAMP |
| payment_method | The total amount paid | DECIMAL(10,2) |
| cogs | Cost Of Goods Sold | DECIMAL(10,2) |
| gross_margin_percentage | Gross margin percentage | FLOAT(11,9) |
| gross_income | Gross Income | DECIMAL(10,2) |
| rating | Rating | FLOAT(2,1) |

---

## 🔍 Analysis List  

### 🛒 Product Analysis  
- Understand different product lines  
- Identify best performing product lines  
- Find product lines that need improvement  

### 💰 Sales Analysis  
- Study sales trends of products  
- Measure effectiveness of sales strategies  
- Suggest modifications to increase sales  

### 👥 Customer Analysis  
- Uncover customer segments  
- Analyze purchase trends  
- Study profitability of each customer segment  

---

## ⚙️ Approach Used  

1. **Data Wrangling**  
   - Inspected data for NULL/missing values  
   - Used NOT NULL constraints in schema design to prevent NULLs  

2. **Build Database**  
   - Created tables and inserted data  

3. **Feature Engineering**  
   - Added new column `time_of_day` → Morning / Afternoon / Evening  
   - Added new column `day_name` → Day of week (Mon, Tue, etc.)  
   - Added new column `month_name` → Month of year (Jan, Feb, etc.)  

4. **Exploratory Data Analysis (EDA)**  
   - Performed queries to answer project business questions  

---

## ❓ Business Questions to Answer  

### General  
- How many unique cities does the data have?  
- In which city is each branch?  

### Product  
- How many unique product lines exist?  
- What is the most common payment method?  
- What is the most selling product line?  
- What is the total revenue by month?  
- Which month had the largest COGS?  
- Which product line had the largest revenue?  
- Which city had the largest revenue?  
- Which product line had the largest VAT?  
- Classify product lines as "Good" or "Bad" depending on sales vs average  
- Which branch sold more products than average?  
- What is the most common product line by gender?  
- What is the average rating of each product line?  

### Sales  
- Number of sales per time of day, per weekday  
- Which customer type brings the most revenue?  
- Which city has the largest VAT %?  
- Which customer type pays the most VAT?  

### Customer  
- How many unique customer types exist?  
- How many unique payment methods exist?  
- What is the most common customer type?  
- Which customer type buys the most?  
- Gender distribution overall and per branch  
- Which time of day customers give most ratings?  
- Which weekday has the best average ratings (overall and per branch)?  

---

## 🧮 Revenue & Profit Calculations  

- **COGS** = unit_price × quantity  
- **VAT** = 5% × COGS  
- **Total (gross sales)** = COGS + VAT  
- **Gross Income** = Total − COGS  
- **Gross Margin %** = Gross Income ÷ Total Revenue  

### Example (from first row in DB):  
- Unit Price = 45.79  
- Quantity = 7  
- **COGS** = 45.79 × 7 = 320.53  
- **VAT** = 5% × 320.53 = 16.0265  
- **Total** = 320.53 + 16.0265 = 336.5565  
- **Gross Margin %** = 16.0265 ÷ 336.5565 ≈ 4.76%  

---

## ✅ Conclusion  
This project explored Walmart sales data using SQL.  
Through feature engineering, EDA, and SQL queries, insights were drawn about:  
- Customer behavior  
- Sales trends  
- Product performance  

These insights can help optimize sales strategies, improve targeting, and boost overall business performance.  
