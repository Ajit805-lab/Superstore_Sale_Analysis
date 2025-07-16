# 📊 Superstore_Sale_Analysis – Power BI Dashboard Project

## 🔍 Overview
    Superstore_Sale_Analysis is an interactive Power Bi dashboard built using a retail dataset to analyze the sales and 
    
    profit trends across different time periods, region, categories. The project provides  key insights into business performance 
    
    and highlights growth opportunities.

## 📁 Dataset Used
    Source: Sample Superstore Dataset(Available via Kaggle)
    
    Data Attributes: Order Date, Sales, Profit, Region, Segment, Category, Sub-Category, city, 
    
    State, Country, Quantity, Discount
    
## 📷 Dataset Overview

<img width="1160" height="652" alt="Screenshot 2025-07-16 095236" src="https://github.com/user-attachments/assets/e314c3a1-530b-4125-82b4-a93a3478cde6" />
    
## 🎯 Objectives
    Compare sales and profit between Q3 and Q4 (2015)

    Identify top-performing categories and underperforming sub-categories

    Visualize regional and segment-wise profit distributions

    Highlight percentage growth or decline in key metrics

    Enable dynamic filtering by Region and Time

## 📊 Key Visualizations
    
    Cards KPIs for Total Sales & Profit in Q3 and Q4
    
    Line Chart Month-wise sales & profit trend comparison
    
    Bar Chart Sub-category wise profit growth (Q4 vs Q3)
    
    Pie / Doughnut Charts Profit breakdown by Category and Segment
    
    Slicers	Region-wise analysis and interactivity
    
## 📈 KPIs Displayed
    🔹 Total_Sale_2015_Q3, Total_Sale_2015_Q4

    🔹 Total_Profit_2015_Q3, Total_Profit_2015_Q4

    🔹 Sale Change %, Profit Change %

## 🎨 Design & Customization

    Color Theme: Blue, Orange, and Green for high visual contrast
    
    Font Style: Modern (e.g., Inter / Segoe UI / Calibri)
    
    Card Titles: Renamed as Sale Change, Profit Change for flexibility (works for both increase and decrease)
    
    Background Color: Light gray #F5F5F5 for modern, distraction-free view
    
    Responsive layout with visual alignment and grid consistency
    
## 🛠️ Data Transformation & ETL process 

#### 🟢 Step 1: Download the Dataset
    Installed the Superstore dataset from Kaggle.

#### 🟢 Step 2: Load Data into Power Query Editor
    Imported the dataset into Power BI and opened it in Power Query Editor for preprocessing.

#### 🟢 Step 3: Data Understanding & Quality Check
    Explored the structure of the dataset.

    Checked column data types, null values, column quality, and column distribution to understand the data.

#### 🟢 Step 4: Data Cleaning & Transformation
    Performed the following steps in Power Query:

    Removed null values and duplicate rows
    
    Renamed columns for clarity
    
    Changed data types appropriately
    
    Created calculated columns (e.g., Year, Quarter, Profit Margin)
    
    Reorganized into a clean tabular format for better analysis

#### 🟢 Step 5: Load Cleaned Data into Power BI Model
    After transformation, loaded the cleaned dataset into Excel sheet

## 🛠 Tools & Technologies
    Power BI Desktop
    
    DAX Measures
    
    Power Query (Data Cleaning)
    
    Basic ETL with filtering, formatting, and type conversion
    
## 📌 DAX Highlights
    Total_Profit = sum(Super_Store1[Profit])
    
    Total_Sale = sum(Super_Store1[Sales])
    
    2015_Q3_Sale = calculate([Total_Sale],YEAR(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=3)
    
    2015_Q4_Sale = calculate([Total_Sale],year(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=4)
    
    2015_Q3_Profit = calculate([Total_Profit] ,year(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=3)
    
    2015_Q4_Sale = calculate([Total_Sale],year(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=4)
    
    Change_profit = Super_Store1[2015_Q4_Profit]-Super_Store1[2015_Q3_Profit]
    
    Change_sale = Super_Store1[2015_Q4_Sale]-Super_Store1[2015_Q3_Sale]
    
    Growth_Q4_vs_Q3_2015_Profit = divide(Super_Store1[2015_Q4_Profit]-Super_Store1[2015_Q3_Profit],Super_Store1[2015_Q3_Profit])*100
    
    Growth_Q4_vs_Q3_2015_sale = divide(Super_Store1[2015_Q4_Sale]-Super_Store1[2015_Q3_Sale],Super_Store1[2015_Q3_Sale])*100
    
## 💡 Insights Uncovered
    🔹 Q4 sales increased by ~40%, with profit up by ~38% compared to Q3.
    
    🔹 Appliances, Copiers, Fasteners, Accessories, Envelopes showed the highest profit growth.
    
    🔹 Blinders, Supplies, Bookcases, Machines, and Storage were the top 5 sub-categories that experienced a negative profit change during the selected period. 
    
    🔹 Consumer segment contributed the largest share of total profit.
    
    🔹 The South region underperformed compared to other regions in terms of sales and profit.
    
## 📬 Contact / Credits
Author: Ajit Kumar Samal

LinkedIn: www.linkedin.com/in/ajitkumarsamal

GitHub: https://github.com/Ajit805-lab

Email: ajitkumarofficial79@gmail.com


       
    
    
      
    
   

 
