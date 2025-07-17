# 📊 Superstore_Sale_Analysis

## 🔍 Overview
    Superstore_Sale_Analysis is an interactive Power Bi dashboard built using a retail dataset to analyze the sales and 
    
    profit trends across different time periods, region, categories. The project provides  key insights into business performance 
    
    and highlights growth opportunities.

## 📁 Dataset Used
    Source: Sample Superstore Dataset(Available via Kaggle)
    
    Data Attributes: Order Date, Sales, Profit, Region, Segment, Category, Sub-Category, city, 
    
    State, Country, Quantity, Discount
    
## 📷 Dataset Overview

<img width="1170" height="625" alt="Screenshot 2025-07-17 100056" src="https://github.com/user-attachments/assets/ffe6fcb2-a13d-4969-859b-5af8acdd0a77" />
    
## 🎯 Objectives
    Compare sales and profit between Q3 and Q4 (2015)

    Identify top-performing categories and underperforming sub-categories

    Visualize regional and segment-wise profit distributions

    Highlight percentage growth or decline in key metrics

    Enable dynamic filtering by Region and Time

## 📊 Key Visualizations
    
#### Cards KPIs for Total Sales & Profit in Q3 and Q4
Sale (Q3 2015)

<img width="319" height="245" alt="Screenshot 2025-07-17 092241" src="https://github.com/user-attachments/assets/2868760f-9cd8-4e20-ba35-9fb1b496ee6d" />

Sale (Q4 2015)

<img width="312" height="254" alt="Screenshot 2025-07-17 092349" src="https://github.com/user-attachments/assets/937bf5d7-8ce8-44fc-8d7e-a0c470ab86bd" />

Sale Change

<img width="312" height="254" alt="Screenshot 2025-07-17 092349" src="https://github.com/user-attachments/assets/76be3da9-9e87-4e2f-a1ea-74586edd52bd" />

Profit (Q3 2015)

<img width="312" height="230" alt="Screenshot 2025-07-17 093220" src="https://github.com/user-attachments/assets/4381aeba-73b4-424d-bde2-a1f4de9cb688" />


Profit (Q4 2015)

<img width="339" height="229" alt="Screenshot 2025-07-17 093253" src="https://github.com/user-attachments/assets/06da4fa1-a931-4251-a29d-c24b4e8ad961" />

Profit Change

<img width="332" height="232" alt="Screenshot 2025-07-17 093329" src="https://github.com/user-attachments/assets/2f0fc2d1-9f47-4ab0-b861-5341bff28f1d" />

#### Line Chart Month-wise sales & profit trend comparison
<img width="774" height="391" alt="Screenshot 2025-07-17 095221" src="https://github.com/user-attachments/assets/6fa657c4-7744-46ca-aec2-419545e2b967" />

#### Bar Chart Sub-category wise profit growth (Q4 vs Q3)
<img width="740" height="493" alt="Screenshot 2025-07-17 095418" src="https://github.com/user-attachments/assets/46dda41e-b1c4-4059-8a6e-dc53ae6f897d" />

#### Doughnut Charts Profit breakdown by Category and Segment
<img width="567" height="402" alt="image" src="https://github.com/user-attachments/assets/7968488d-db7d-44d6-8e88-26a6631f4775" />

#### Pie Charts Profit breakdown by Category and Segment
<img width="515" height="425" alt="Screenshot 2025-07-17 095748" src="https://github.com/user-attachments/assets/52bc0927-c6f6-4ff2-a504-b0ab9de872f6" />

## 📈 KPIs Displayed
    🔹 Sale (Q3 2015), Sale (Q4 2015)

    🔹 Profit (Q3 2015), Profit (Q4 2015)

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
    Total_Sale = sum(Super_Store1[Sales])
    
    Total_Profit = sum(Super_Store1[Profit])
    
    Sale(Q3 2015) = calculate([Total_Sale],YEAR(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=3)

    Sale(Q4 2015) = calculate([Total_Sale],year(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=4) 
     
    Profit(Q3 2015) = calculate([Total_Profit] ,year(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=3)
    
    Profit(Q4 2015) = calculate([Total_Profit] ,year(Super_Store1[Order Date])=2015,Super_Store1[Quarter]=4)
    
    Change_sale = Super_Store1[Sale(Q4 2015)]-Super_Store1[Sale(Q3 2015)]
    
    Change_profit = Super_Store1[Profit(Q4 2015)]-Super_Store1[Profit(Q3 2015)]

    Growth_Q4_vs_Q3_2015_sale = divide(Super_Store1[Sale(Q4 2015)]-Super_Store1[Sale(Q3 2015)],Super_Store1[Sale(Q3 2015)])
    
    Growth_Q4_vs_Q3_2015_Profit = divide(Super_Store1[Profit(Q4 2015)]-Super_Store1[Profit(Q3 2015)],Super_Store1[Profit(Q3 2015)])
    
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


       
    
    
      
    
   

 
