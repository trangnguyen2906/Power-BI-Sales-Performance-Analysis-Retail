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

![Dashboard Walkthrough](https://drive.google.com/uc?export=view&id=1HyZkhunpnyqoVN_bR2zvdNqDOZjFgouG)

### 📌 Analysis 1:  

To understand overall business health, I started with an executive-level view of key metrics including:  
💰 **Total Profit:** $1.5M 📦 **Total Sales:** $12.64M 📄 **Total Orders:** 25.04K 📈 **% Profit:** 11.61% 📦 **% Return Rate:** 5.95%

From the visualizations, I observed the following:

### 🔍 1. Sales Performance Is Strong, but Margins Are Modest  
- **💡 Observation:**
Total **sales** reached **$12.64M**, but only **$1.5M in profit** was generated, resulting in a **profit margin of 11.61%**. This shows that high sales volume does not directly translate into high profitability, possibly due to cost structure or product mix.

- **✅ Recommendation:**
Prioritize margin optimization by identifying high-volume but low-profit products. Review pricing strategies, reduce discount dependency, and streamline costs to protect profitability without sacrificing sales volume.

### 🔍 2. Consistent Seasonal Trends
- **💡 Observation:**
Each year, **Q1 consistently shows the lowest sales and profit**, but performance **steadily improves through Q2–Q4**, with the highest **peak in Q4 2014 ($1.48M)**. Despite these seasonal dips, the overall trend in both sales and profit is **upward**, indicating healthy business momentum.

- **✅ Recommendation:**
Mitigate Q1 drops by launching retention-focused campaigns early in the year, offering loyalty incentives, and planning proactive inventory and pricing strategies ahead of Q3, Q4 to capture peak demand efficiently.

### 🔍 3. Sub-Category Profitability Varies Widely
- **💡 Observation:**
 + **Technology** is the top-performing category: 📠 **Copiers** and 📱 **Phones** show strong sales and high profits, while **Accessories** also perform well.
 + **Office Supplies** has the **highest margin sub-category** — 📎 **Paper (24.24%)**, but most others (e.g., Binders, Envelopes) contribute low profit due to small sales.
 + **Furniture** underperforms overall: 🪑 Tables have a **negative margin (-8.46%)**, and while 📚 **Bookcases** and **Chairs** generate decent sales, their margins **(11–12%) are below other categories.**

- **✅ Recommendation:**
  + Double down on Technology and Paper through bundling or cross-sell. 
  + Investigate the viability of low-performing products like Tables and Envelopes, whether due to pricing, high returns, or low demand—and consider repositioning, redesigning, or phasing them out.

### 🔍 4. Consumer Leads in Sales, but Home Office Delivers Highest Margin
- **💡 Observation:**
  + **Consumer segment** generates the **highest revenue** at $6.5M, but yields the lowest profit margin (11.51%).
  
  + Home Office is the smallest segment by sales ($2.3M) but delivers the **highest profit margin (11.99%)**.

- **✅ Recommendation:**
Reinforce engagement with Home Office customers through premium or recurring offerings. Explore ways to increase volume in this segment while protecting margins. Simultaneously, analyze costs and pricing in the Consumer segment to improve margin without sacrificing scale.

### 🔍 5. APAC Leads in Sales, Followed by Europe, US, and LATAM
- **💡 Observation:**
**APAC** drives the highest sales volume, followed by **Europe**. The **US and LATAM** are close behind, while **Africa, EMEA (non-EU), and Canada** remain **low** in both presence and volume. As the chart reflects sales only, profitability must be evaluated using other visuals.
  
- **✅ Recommendation:**
Sustain growth in APAC, Europe, and the US through focused operations and optimization. For emerging markets such as LATAM and Africa, refer to margin data from Page 2 to identify where lean expansion or pilot initiatives may yield strategic growth.


### 2️⃣ Strategic Product & Market Insights - Preview  

![Technology Region Profit Margin](https://drive.google.com/uc?export=view&id=1KEXVnHP2fSkRdtrnt3_eozf3O31Pv2Ab)


### 📌 Analysis 2:   
  
### 🔍 **Technology – High Revenue Driver with Uneven Product & Market Outcomes**
- Technology is the **top-performing category**, generating **$4.74M in revenue** and contributing **$663.8K in profit**, with a solid **margin of 13.99%**. However, this strong overall performance masks wide **variation** between **sub-categories and regions**.

- The top sub-categories include:

+ **📠 Copiers:** $258.6K profit, 17.13% margin
+ **🧩 Accessories:** $129.2K profit, 17.3% margin
+ **📱 Phones:** $216.7K profit, 12.7% margin

These high-margin products drive most of the category’s success and are particularly strong in regions like **Central EU, North Asia, and the US.**

- ⚠️ However, **Machines** remain a weak spot, with the **lowest margin (7.56%)**. Many low-performing SKUs (e.g., Zebra, Lexmark, Okidata) appear in the top loss-making list, especially in countries such as **Turkey, Nigeria, and the Netherlands**.
- ⚠️ Meanwhile, Canada emerges as a margin outlier,despite its low sales volume, it delivers the **highest profit margin** of all regions, suggesting strong operational efficiency and potential for targeted expansion.
- ❗ Losses are concentrated in Africa, EMEA, and parts of LATAM, often tied to low-efficiency Machines and Copiers.

### **✅ Recommendation:**

- **Expand Copiers, Accessories, and Phones** in high-performing regions such as **Central EU, North Asia, and the US**, where both volume and margin potential are proven.

- **Conduct a SKU-level audit** of the Machines sub-category, especially in underperforming countries like Turkey, Nigeria, and the Netherlands. Prioritize phasing out or rebranding low-efficiency products.

- **Leverage Canada** as a high-margin testbed for premium tech offerings. Despite its small size, its operational efficiency makes it ideal for pilot campaigns or bundling strategies.

- In low-performing markets like **Africa, EMEA, and parts of LATAM**, **avoid expanding Machines**, and instead introduce high-margin, low-risk products like **Accessories** through lean, targeted rollouts.


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
