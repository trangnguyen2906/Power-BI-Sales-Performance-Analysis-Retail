# 📊 Analyze Sales Performance on Superstore Dataset Using Power BI

## 📑 Table of Contents  
1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---

## 📌 Background & Overview  

### 🎯 Objective:
### 📖 What is this project about? 

This project analyzes global retail sales using the **Global Superstore** dataset and **Power BI**. It is designed to help senior managers:

- Understand **sales and profit performance** across regions and products.

- Identify **strategic opportunities** and **loss drivers**.

- Make data-informed decisions on **product prioritization and market expansion.**

### ❓ Business Questions

This project helps answer key business questions, such as:

- Which regions and markets are most/least profitable?

- What product categories and sub-categories drive sales and returns?

- Which customer segments yield the highest profit?

- What factors are contributing to high return rates?


### 👥 Who is this project for?

- Business stakeholders and senior managers  
- Sales & marketing strategy teams  
- Data analysts and business intelligence professionals  


---

## 📂 Dataset Description & Data Structure  

### 🔗 Data Source

- **Source**: Global Superstore dataset
- **Size**: ~51,920 rows
- **Format**: `.csv` file
  
### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used:  

The dataset includes **3 tables**:

1. **Orders** – Main transactional table (sales, profit, shipping, customer info)  
2. **Returns** – Links to Orders to flag returned transactions  
3. **People** – Sales representatives and their assigned regions  


#### 2️⃣ Table Schema & Data Snapshot  

<details>
<summary><strong>📦 Orders Table </strong></summary>

_This table contains sales transactions and business metrics._

| Column Name     | Data Type | Description                        |
|------------------|-----------|------------------------------------|
| Order ID         | TEXT      | Unique identifier for each order   |
| Order Date       | DATE      | Date when order was placed         |
| Ship Date        | DATE      | Shipping date                      |
| Product ID       | TEXT      | Product code                       |
| Product Name     | TEXT      | Name of the product                |
| Category         | TEXT      | Main product category              |
| Sub-Category     | TEXT      | Detailed product category          |
| Sales            | FLOAT     | Sales amount                       |
| Profit           | FLOAT     | Profit earned                      |
| Quantity         | INT       | Number of items sold               |
| Segment          | TEXT      | Customer segment (e.g. Consumer)   |
| Region           | TEXT      | Sales region                       |
| Market           | TEXT      | Geographical market zone           |
| Ship Mode        | TEXT      | Shipping type                      |
| State / Country  | TEXT      | Geolocation                        |
| Returns.Returned | BOOLEAN   | Indicates if order was returned    |

</details>



<details>
<summary><strong>♻️ Returns Table</strong></summary>

_This table flags which orders were returned._

| Column Name | Data Type | Description                         |
|-------------|-----------|-------------------------------------|
| Order ID    | TEXT      | Linked Order ID from Orders table   |
| Returned    | BOOLEAN   | Return status                       |

</details>



<details>
<summary><strong>👤 People Table</strong></summary>

_Contains sales representative details per region._

| Column Name | Data Type | Description                    |
|-------------|-----------|--------------------------------|
| Person      | TEXT      | Sales rep name                 |
| Region      | TEXT      | Sales region assigned          |

</details>

#### 3️⃣ Data Relationships:  

<img src="https://drive.google.com/uc?export=view&id=1C5VlvfroFiQDeeaMUa9JrUfSzglpjMyk" width="700"/>

---

## 🧠 Design Thinking Process 

This project leveraged **Design Thinking process** to deeply explore stakeholder needs and shape a focused dashboard that supports strategic decision-making.

### 1️⃣ **Empathize :** 
Understand the real needs and expectations of senior managers, especially the CSO, who are responsible for making strategic product and market expansion decisions.

![Design Thinking Screenshot](https://drive.google.com/uc?export=view&id=1QmYiExV79vE1s7Z8mCcyhfRfj04Fmsbp)

![Strategic Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1duTmMTQU7rxtSOuCLKyvguwg2gBn3p8l)


### 2️⃣ **Define point of view:** 
I defined the problem as the lack of a centralized, visual dashboard to track profit, return, and growth across regions and products.

![Customer Pattern Screenshot](https://drive.google.com/uc?export=view&id=1ZVKmTq3dH-rEwqnC0cCuyva9m36ixw1r)

### 3️⃣ **Ideate:** 
I designed a 4-page dashboard structure that covers financial overview, product-market insights, customer behavior.

![Recommendations & Insights Screenshot](https://drive.google.com/uc?export=view&id=14xy-wXt4yCpPTSaYrxZPrNLZDwP4nZgv)


### 4️⃣ **Prototype and review:**

I built the dashboard in Power BI and reviewed it to ensure it answers key stakeholder questions effectively. Then, I reviewed it through the lens of the stakeholder questions and refined the visuals to ensure they deliver clear insights for strategic action.

---

## ⚒️ Main Process

### 1️⃣ Data Preprocessing (Power Query + DAX)
- Connected to Superstore source files (Orders, People, Returns) in Power BI.
- Cleaned and transformed data using **Power Query Editor**:
 + Used first row as headers, changed data types, and **removed/replaced invalid values.**
 + **Merged tables** (e.g., Orders + Returns) to track return status per transaction.
 + **Added custom columns** to flag returned orders and calculate profit margins.
 + **Reordered and renamed columns** for consistency and ease of use.
- Built a **relational data model** by creating relationships among the tables.
- Created essential DAX measures and calculated columns for key metrics: `Total Profit`, `% Return`, `Sales Growth`, `AOV`,...


### 2️⃣ Power BI Visualization
Developed a multi-page interactive dashboard in Power BI with filters and KPIs, focusing on strategic decision-making.

Each page answers specific stakeholder questions:

- **Page 1 –** **Business Overview:** Financial health, sales trends, profit by different dimensions.

- **Page 2 –** **Product & Market Insights:** Top/bottom products, profitable countries, product-level profit margin.

- **Page 3 –** **Customer Patterns & Risks:** Return analysis, shipping behavior, customer segmentation.

---

## 📊 Key Insights & Visualizations  
 

### 1️⃣ Page 1: Business Performance Overview - Preview  

![Page 1](https://drive.google.com/uc?export=view&id=1QEGmvNWgRN2YPpMON9bDsYdLTvL-y6_L)

### 📌 Analysis 1:  

To understand overall business health, I started with an executive-level view of key metrics including:  
💰 **Total Profit:** $1.5M 📦 **Total Sales:** $12.64M 📄 **Total Orders:** 25.04K 📈 **% Profit:** 11.61% 📦 **% Return Rate:** 5.95%


#### 🔍 1. Sales Performance Is Strong, but Margins Are Modest  

### 2️⃣ Dashboard 2 Preview  


📌 Analysis 2:   
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

### 3️⃣ Dashboard 3 Preview  


📌 Analysis 3:  
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

---

## 🔎 Final Conclusion & Recommendations  

👉🏻 Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:  

📌 Key Takeaways:  
✔️ Recommendation 1  
✔️ Recommendation 2  
✔️ Recommendation 3
