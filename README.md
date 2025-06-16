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

### 👥 Who is this project for?

- Business stakeholders and senior managers  
- Sales & marketing strategy teams  
- Data analysts and business intelligence professionals  


### ❓ Business Questions
This project helps answer key business questions, such as:

- Which regions and markets are most/least profitable?

- What product categories and sub-categories drive sales and returns?

- Which customer segments yield the highest profit?

- What factors are contributing to high return rates?



### 🎯 Project Outcome:

Summarized below are key findings and patterns uncovered through analysis:


✔️ Sales Trends: The top X% of products generate Y% of revenue.  
✔️ Inventory Optimization: Certain products are frequently out-of-stock, causing revenue loss.  
✔️ Customer Behavior: Returning customers spend Z% more per transaction than new customers.  

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
<summary><strong>📦 Orders Table</strong></summary>

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
Describe the connections between tables—e.g., one-to-many, many-to-many.  

👉🏻 Include a screenshot of Data Modeling to visualize relationships.  

---

## 🧠 Design Thinking Process  

Explain the step-by-step approach taken to solve the problem.  

👉🏻 Insert a screenshot of the Design Thinking steps (Screenshot your Excel design thinking tables for better presentation).  

1️⃣ Empathize  
2️⃣ Define point of view  
3️⃣ Ideate  
4️⃣ Prototype and review  

---

## ⚒️ Main Process

1️⃣ Data Cleaning & Preprocessing  
2️⃣ Exploratory Data Analysis (EDA)  
3️⃣ SQL/ Python Analysis 

- In each step, show your Code

- Include query/ code execution screenshots or result samples

- Explain its purpose and its findings


4️⃣ Power BI Visualization  (applicable for PBI Projects)

---

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  

![Image Description](https://drive.google.com/uc?export=view&id=1F2GZEVsQiCMnXISj0Hmhqtp12cfGaYLR)

📌 Analysis 1:  
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

#### 2️⃣ Dashboard 2 Preview  


📌 Analysis 2:   
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

#### 3️⃣ Dashboard 3 Preview  


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
