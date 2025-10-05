# Python_Diwali_Sales_Analysis
Python project for beginners- Analyze Diwali sales data to improve customer experience and sales

# Diwali Sales Analysis (Python)

Analyze Diwali-season retail data to uncover customer segments, top-performing product categories, and sales opportunities — all in a single Jupyter notebook.

---

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a Diwali sales dataset to:

* Clean and prepare raw data
* Explore **customer demographics** (gender, age group, marital status, state, occupation)
* Analyze **orders, revenue, and product categories**
* Visualize insights that can guide **marketing and inventory** decisions

---

## 🗂 Repository Structure

```
.
├── Diwali_Sales_Analysis.ipynb   # Main analysis notebook
├── Diwali Sales Data.csv         # Input dataset
└── README.md                     # You are here
```
---

## ▶️ How to Run

1. Open `Diwali_Sales_Analysis.ipynb`.
2. Ensure the CSV path matches your environment (same folder is simplest).
3. Run cells top-to-bottom.
4. Explore and tweak plots/filters to answer your own business questions.

---

## 🧹 Data Cleaning (What the notebook does)

Typical steps in the notebook include:

* Removing null/blank rows in key numeric columns (e.g., `Amount`, `Orders`)
* Converting dtypes (e.g., `Amount` to numeric)
* Standardizing categories (e.g., age groups, product categories)
* Deriving KPI fields (e.g., total spend by segment)

> These steps are performed in the provided notebook to prepare the dataset for EDA. ([GitHub][2])

---

## 🔎 Exploratory Analysis & Visuals

The notebook explores (and you can extend):

* **Customer profile**: distribution by **Gender**, **Age Group**, **Marital Status**, **Occupation**, **State**
* **Sales performance**: **Orders** & **Amount** by demographic segment and **Product Category**
* **Top performers**: best-selling **states**, **categories**, and **products**

> The upstream project focuses on EDA and visualization to improve customer experience and sales planning.

---

## 💡 Example Questions You Can Answer

* Which **age group** contributes the highest revenue?
* Do **married** customers spend more on average?
* Which **states** lead in orders vs. revenue?
* What **product categories** peak during Diwali?
* Are there **gender** or **occupation** segments worth targeted campaigns?

---

## 📈 Sample Code Snippets

**Top states by revenue**

```python
(
    df.groupby("State", as_index=False)["Amount"]
      .sum()
      .sort_values("Amount", ascending=False)
      .head(10)
)
```

**Orders & revenue by customer segment**

```python
(
    df.groupby(["Gender", "Age Group"], as_index=False)
      .agg(Orders=("Orders","sum"), Revenue=("Amount","sum"))
      .sort_values("Revenue", ascending=False)
)
```

**Category contribution**

```python
(
    df.groupby("Product_Category", as_index=False)["Amount"]
      .sum()
      .sort_values("Amount", ascending=False)
)
```

---

## 🧭 Extend the Project

* Add a **requirements.txt** and pin versions for reproducibility
* Build **interactive dashboards** (Streamlit/Plotly Dash)
* Create a **segmentation** view (e.g., RFM analysis)
* Add **statistical tests** (e.g., spend differences by segment)
* Export an **executive summary** (top 5 insights + suggested actions)

---


## 🔒 License

The upstream repository does not list a license file. If you intend to reuse/redistribute, consider adding a suitable open-source license (e.g., MIT/Apache-2.0) to clarify terms. 


[4]: https://www.youtube.com/watch?v=KgCgpCIOkIs&utm_source=chatgpt.com "Python Project for Data Analysis- Exploratory Data Analysis ..."
[5]: https://github.com/rishabhnmishra?utm_source=chatgpt.com "Rishabh Mishra rishabhnmishra"
