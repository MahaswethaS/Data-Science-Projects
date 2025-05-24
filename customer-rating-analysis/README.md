Customer Rating Analysis
**Project Overview**
This project explores customer satisfaction across 14 product categories from an e-commerce(FlipKart) dataset from Kaggle.
The analysis aims to determine whether differences in average product ratings are statistically significant, 
using robust statistical tests that account for real-world data challenges like unequal variances and sample sizes.

**Summary**
1. Data cleaning
   1.1 Product Categorization:The original dataset lacked a proper product category column, which was essential for group-wise statistical analysis.
       To address this:
        I manually defined 14 product categories based on the nature and purpose of items.
        Then, I used a custom function and a loop to assign each product to its respective category by checking for relevant keywords in the product name.
        This ensured that all products were consistently and meaningfully categorized, enabling valid group comparisons during statistical testing.
   1.2 Price Column Cleaning
   Removed unwanted characters (like ₹, commas) using regex
2. Statistical Analysis
   2.1 Welch's Annova (This is used due to unequal sample sizes and variance)
       Result: p < 0.001 → Significant differences in category ratings.
   2.2 Games-Howell Post Hoc Test:
       After discovering that group means differ, I ran a Games-Howell post hoc test to identify which specific pairs of categories were significantly different.

**Conclusion**
Welch’s ANOVA confirmed that product categories differ significantly in their customer ratings (p < 0.001).
Games-Howell revealed which category pairs had statistically significant differences in average ratings (using a significance threshold of 0.05).
This allows us to draw category-level insights into customer preferences — crucial for marketing strategy, pricing, and product planning.
   





