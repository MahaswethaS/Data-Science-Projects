# Customer Rating Analysis Project Overview

This project explores customer satisfaction across **14 product categories** from an e-commerce (Flipkart) dataset hosted on Kaggle.  
The analysis aims to determine whether differences in average product ratings are **statistically significant**, using robust tests that account for **unequal variances** and **sample sizes**.

---

## Summary

### 1. Data Cleaning

#### 1.1 Product Categorization
The original dataset lacked a proper product category column, which was essential for group-wise statistical analysis.  
To address this:

- I **manually defined 14 product categories** based on the nature and purpose of items.
- Then, I used a **custom function and a loop** to assign each product to its respective category by checking for **relevant keywords in the product name**.

This ensured that all products were **consistently and meaningfully categorized**, enabling valid group comparisons during statistical testing.

#### 1.2 Price Column Cleaning
- Removed unwanted characters (like `₹`, commas) using **regex**.
- Converted the cleaned column to **numeric format**, dropping nulls.

---

### 2. Statistical Analysis

#### 2.1 Welch's ANOVA
- Used due to **unequal sample sizes and variance** across product categories.
- **Result**: `p < 0.001` → **Significant differences in category ratings**.

#### 2.2 Games-Howell Post Hoc Test
- After detecting overall differences, I ran **Games-Howell** to find **which specific category pairs** differ.
- This test handles **heteroskedasticity** and **unbalanced group sizes**.

---

## Conclusion

- **Welch’s ANOVA** confirmed that **product categories differ significantly** in their customer ratings (`p < 0.001`).
- **Games-Howell** revealed which **category pairs** had statistically significant differences in average ratings (with a threshold of `p < 0.05`).

These findings enable **category-level insights into customer preferences** — crucial for:
- Product planning
- Pricing strategy
- Targeted marketing

---
