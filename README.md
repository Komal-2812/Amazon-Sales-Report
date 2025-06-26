📊 Amazon Sales Report Dashboard – Power BI

📁 Project Overview
This interactive Power BI dashboard provides a comprehensive analysis of Amazon marketplace sales. 
It is designed for business stakeholders to gain insights into sales performance, customer behavior, and product trends.

 ⚠️ **Note:** The original `.csv`("Amazon Sale Report.csv" :- Kaggel) dataset could not be uploaded directly due to its large size. 
 Instead, all relevant data has been imported and modeled directly in the `.pbix` file.

 🧱 File Information
 **File Name:** `Amazon Sales report.pbix`
 **Pages in Report:**
   Page 2: Sales Report
   Page 3: Customer Analysis
   Page 4: Product Analysis

 Page 2: Sales Report
🎯 Objective:
Gain a snapshot of key sales KPIs, regional performance, and order trends.
 📊 Visuals:
 **KPI Cards** – Total Sales, Orders, Quantity, Avg Order Value
 **Line Chart** – Sales over Time (`date`)
 **Bar Chart** – Sales by Country (`ship_country`)
 **Slicers** – `date`, `category`, `fulfilment`, `ship_country`

 🔹 Page 3: Customer Analysis
 🎯 Objective:
Analyze customer distribution, delivery performance, and order behavior.
 📊 Visuals:
 **Bar Charts** – Orders by City and State
 **Donut Chart** – Courier Status Breakdown
 **Map** – Sales by City
 **Slicers** – `shipstate`, `courier status`, `fulfilment`, 

 🔹 Page 4: Product Analysis
 🎯 Objective:
Understand which products, categories, and SKUs drive sales and volume.
 📊 Visuals:
 **Bar Charts** – Sales by Category, Top SKUs
 **Column Chart** – Sales by Style
 **Pie Chart** – Quantity Sold by Size
 **Slicers** – `category`, `style`,

📈 DAX Measures Used
DAX
Total Sales = SUM(AmazonSales[amount])
Total Orders = DISTINCTCOUNT(AmazonSales[orderid])
Total Quantity = SUM(AmazonSales[oty])
Avg Order Value = DIVIDE([Total Sales], [Total Orders])
Sales Prev Month = CALCULATE([Total Sales], PREVIOUSMONTH(AmazonSales[date]))
MoM Growth % = DIVIDE([Total Sales]  [Sales Prev Month], [Sales Prev Month])

