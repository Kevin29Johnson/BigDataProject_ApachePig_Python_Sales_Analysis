# 🛒 eCommerce Sales Analysis - ETL Pipeline with Apache Hadoop & Pig

<div align="center">
  <img src="https://img.shields.io/badge/Apache%20Hadoop-66CCFF?style=for-the-badge&logo=apachehadoop&logoColor=black" alt="Hadoop"/>
  <img src="https://img.shields.io/badge/Apache%20Pig-FF6B6B?style=for-the-badge&logo=apache&logoColor=white" alt="Pig"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
</div>

## 📊 Project Overview

Comprehensive **ETL pipeline** analyzing Big Basket's eCommerce dataset using **Apache Hadoop** for distributed storage, **Apache Pig** for large-scale processing, and **Python/Pandas** for data cleaning.

**Data Source**: [Kaggle - Big Basket Products Dataset](https://www.kaggle.com/hetulmehta/bigbasket-products-dataset)

---

## 🏗️ Architecture & Data Flow
📥 Raw Data (Kaggle) → 🐍 Python/Pandas (Clean) → 🐘 Hadoop HDFS (Store) → 🐷 Apache Pig (Analyze) → 📊 Insights

**Schema**: Product, Category, Sub-Category, Brand, Type, Rating, Sale_Price, Market_Price, Profit, Profit%

---

## 🧹 Data Cleaning & Processing

### **Python/Pandas Cleaning:**
- ✅ Removed unnecessary columns (URLs, codes)
- ✅ Handled null values (median imputation for ratings)
- ✅ Removed duplicates and standardized data types
- ✅ **Result**: 95%+ data quality after cleaning

### **Apache Pig Analytics:**
```pig
-- Load cleaned data
project = LOAD '/home/kevin/Desktop/new.csv' USING PigStorage(',') 
          AS (product:chararray, category:chararray, brand:chararray, 
              rating:float, sale_price:float, profit:float);

-- Maximum rated products (Rating = 5)
temp1 = FILTER project BY rating==5.0;

-- Brand-wise product count
gbrand = GROUP project BY brand;
cnt_prod = FOREACH gbrand GENERATE group, COUNT(project);

-- Most profitable product
h1 = GROUP project ALL;
l = FOREACH h1 GENERATE MAX(project.profit) AS max;
x = FILTER project BY profit==l.max;

```

## 📊 Key Insights & Findings
🏆 Product Performance:

Highest Rated (5.0): Drinks (Tea), Sanitary products, Baby care items
Lowest Rated (1.0): Beauty, skin-care, hygiene products
Most Profitable: Premium Cloth Dryer (₹4,649 profit)
Most Expensive: Epilator (₹10,769)
Cheapest: Curry Leaves (₹12.55)

## 🏢 Brand Analysis:

Top Brands by Count: Fresho, BB Home, Colgate
Highest Rated: Mars and Nice (5.0 average)
Popular: Oreo, Tang (4.0 average)

## 📈 Business Recommendations:

Marketing Focus: Promote low-rated cleaning/household products
Pricing Strategy: Optimize fruits/vegetables pricing (low profit)
Quality Improvement: Address beauty/skincare product issues
Inventory Priority: Focus on high-profit Beauty & Hygiene categories


## 🎯 Key Takeaways

Big Data ETL: End-to-end pipeline with Hadoop ecosystem
Data Quality: Comprehensive cleaning and validation
Business Intelligence: Actionable insights from eCommerce data
Scalability: Handles large datasets efficiently
