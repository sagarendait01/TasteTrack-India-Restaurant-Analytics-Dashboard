# 🍽️ DineInsight India — Restaurant Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge\&logo=powerbi\&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data%20Analysis-blue?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Transformation-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

> **An interactive Power BI dashboard for analyzing Indian restaurant data across cities, cuisines, ratings, cost and customer votes.**

---

## 📌 Project Overview

**DineInsight India** is a Power BI analytics project created to understand restaurant data from different business perspectives.

My goal was not just to create charts, but to build a logical analytical flow from **restaurant location and cuisine to ratings, pricing, popularity and individual restaurant details**.

### 🔄 Analytical Flow

**City → Cuisine → Rating → Cost → Votes → Restaurant Details**

The dashboard helps answer questions such as:

* Which cities have more restaurants?
* What cuisines are represented in the dataset?
* How are restaurants distributed across rating bands?
* What cost-for-two ranges are common?
* How does restaurant cost relate to customer votes?
* Which individual restaurants are behind the numbers?

---

# 📊 Dashboard Overview

The report is organized into **3 analytical pages**.

### 1️⃣ City & Cuisine Overview

This page focuses on the geographical and cuisine perspective.

**Key analysis:**

* Restaurant count by city
* Cuisine-wise restaurant analysis
* City and Cuisine filtering

The objective is to understand **where restaurants are concentrated and what cuisine categories are present**.

---

### 2️⃣ Rating & Cost Distribution

This page focuses on restaurant ratings and pricing.

**Key analysis:**

* Rating distribution using rating bands
* Cost-for-two distribution using cost bands
* Restaurant count across different rating and cost ranges

This helps understand the **quality and pricing distribution** within the selected restaurant segment.

---

### 3️⃣ Restaurant Deep Dive

The third page combines multiple variables for deeper analysis.

**Key analysis:**

* Cost vs Votes
* Rating
* City-wise comparison
* Restaurant-level details

The scatter analysis helps explore the relationship between **restaurant cost and customer popularity**, where votes represent customer engagement.

The detailed table provides:

| Field   | Description              |
| ------- | ------------------------ |
| Name    | Restaurant name          |
| City    | Restaurant location      |
| Cuisine | Cuisine type             |
| Rating  | Restaurant rating        |
| Votes   | Number of customer votes |
| Cost    | Approximate cost for two |

---

# 🎛️ Interactive Features

The dashboard includes interactive **City** and **Cuisine** slicers.

When a selection is made, the report updates according to the selected filter context.

### Example

If I select:

**City → Pune**

and

**Cuisine → Fast Food, Desserts**

I can then analyze:

**Restaurant Count → Rating → Cost → Votes → Restaurant Details**

This allows the dashboard to move from a high-level overview to a more detailed restaurant-level analysis.

---

# 🧮 DAX Measures

I used DAX to create custom calculations for the dashboard.

### Restaurant Count

```DAX
Count =
COUNTROWS(restaurants)
```

This measure counts the restaurant records available in the current filter context.

### Cuisine Analysis

```DAX
Cuisine Restaurant Count =
DISTINCTCOUNT(restaurants[Cuisine])
```

This measure counts distinct cuisine values in the current filter context.

---

# 🔍 Data Profiling & Quality Checks

Along with dashboard development, I also used DAX queries to understand the quality and structure of the data.

The analysis included checks such as:

* Total count
* Distinct values
* Null count
* Minimum value
* Maximum value
* Mean
* Median
* Standard deviation
* Percentile analysis

This helped me understand the dataset before using it for visualization and analysis.

---

# 🧱 Data Model

The report is built around a single table:

### `restaurants`

| Column          | Type    | Purpose                  |
| --------------- | ------- | ------------------------ |
| `Name`          | Text    | Restaurant name          |
| `City`          | Text    | Restaurant city          |
| `Cuisine`       | Text    | Cuisine category         |
| `Rating`        | Decimal | Restaurant rating        |
| `Votes`         | Number  | Customer votes           |
| `Cost`          | Number  | Approximate cost for two |
| `Rating (bins)` | Grouped | Rating bands             |
| `Cost (bins)`   | Grouped | Cost brackets            |

---

# 🛠️ Technology Stack

### Power BI Desktop

Used for:

* Dashboard development
* Data visualization
* Interactive filtering
* Report design

### DAX

Used for:

* Custom measures
* Restaurant counting
* Distinct cuisine analysis
* Data profiling and analytical calculations

### Power Query

Used for:

* Data preparation
* Data transformation
* Creating analytical fields/bins

---

# 📁 Repository Structure

```text
DineInsight-India/
│
├── Indian_Restaurant_Data_Analytics.pbix
├── Indian_Restaurant_Data_Analytics.pdf
│
├── data/
│   └── restaurants_dataset.*
│
├── README.md
└── LICENSE
```

> The `data` folder is optional and should only be included if the dataset can be legally shared.

---

# ⚙️ How to Use the Project

## Prerequisites

* Microsoft Power BI Desktop
* Windows
* Optional: Power BI Service for online publishing

## Open the Dashboard

1. Clone or download this repository.
2. Open `Indian_Restaurant_Data_Analytics.pbix` in Power BI Desktop.
3. Refresh the data if required.
4. Use the **City** and **Cuisine** slicers.
5. Navigate through the three report pages.
6. Explore the charts and restaurant-level details.

---

# 📄 Dashboard Preview

The repository also contains:

**`Indian_Restaurant_Data_Analytics.pdf`**

This PDF provides a visual export of the three Power BI dashboard pages.

---

# 💡 Key Learning

This project helped me understand that a good dashboard is not only about creating attractive visuals.

The important part is creating a **logical connection between the data, analysis and business questions**.

For this project, I followed the flow:

> **Where are the restaurants?**
> ↓
> **What cuisines do they offer?**
> ↓
> **How are they rated?**
> ↓
> **What is their cost?**
> ↓
> **How popular are they based on votes?**
> ↓
> **Which restaurants are behind the numbers?**

This approach helped me improve my skills in **Power BI, DAX, data visualization, data preparation and analytical thinking**.

---

# 🎯 Project Objective

The overall objective of **DineInsight India** is to convert restaurant-level data into an interactive analytical view that makes it easier to understand:

**Restaurant Distribution + Cuisine + Rating + Pricing + Popularity**

---

# 👨‍💻 About Me

**Sagar Endait (DA)**
Data Analyst | Power BI | DAX | Data Analytics

I am building projects to strengthen my practical understanding of **data analysis, business intelligence and visualization**.

---


# 📜 License

This project is licensed under the **MIT License**.

---

⭐ **If you found this project useful, consider giving the repository a star!**
