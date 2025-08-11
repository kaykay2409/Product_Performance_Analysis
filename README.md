# Amazon_Product_Performance_Analysis
A dashboard project analyzing product and review data from Amazon. This project uses pivot tables, calculated columns, and charts to generate insights that support product improvement, marketing strategies, and customer engagement.
## Amazon_Product Performance Analysis
Junior Data Analyst at RetailTech Insight

#

## Project Summary
As part of the analytics team at RetailTech Insights, I was tasked with analyzing Amazon product and customer review data. The goal was to generate insights that can guide:
- Product improvement
- Marketing strategies
- Customer engagement

#

## Project Objectives
To analyze product and review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

#

## Dataset Description
- Total Records: 1,465 rows
- Total Columns: 16
- Each row = 1 product
- Data includes: product names, categories, prices, discounts, ratings, reviews, etc.

#

## Tools Used
### Microsoft Excel for:
- Data cleaning
- Calculated columns
- Pivot Tables & Charts
- Dashboard

#

### Data Cleaning (in Excel)
- Changed data types to appropriate formats (e.g., number, text)
- Split the category column for consistency
- Removed 64 duplicate rows
- Corrected spelling errors
- Applied Proper Case formatting for readability
- Removed blank rows using filters

#

## Questions and Analysis
**1. What is the average discount percentage by product category?**
- Rows: category
- Values: discount_percentage → Average
- Insight: Identify which categories give the highest average discounts.

  <img width="405" height="195" alt="image" src="https://github.com/user-attachments/assets/bf969475-c36c-4c6e-add7-9419582c05ea" />


**2. How many products are listed under each category?**
- Rows: category
- Values: product_name → Count (or count of products)
- Insight: Understand product spread across categories.

   <img width="261" height="194" alt="image" src="https://github.com/user-attachments/assets/574e754d-3d41-4209-bd99-005311ca5799" />


**3. What is the total number of reviews per category?**
- Rows: category
- Values: rating_count → Sum
- Insight: See which categories drive the most customer interaction.

  

**4. Which products have the highest average ratings?**
- Rows: product_name
- Values: rating → Max or Average
- Sort Descending
-Insight: Surface top-performing products.

**5. What is the average actual price vs discounted price by category?**
- Rows: category
- Values: actual_price → Average
- Values: discounted_price → Average
- Insight: Compare real prices with offered deals across categories.

**6. Which products have the highest number of reviews?**
- Rows: product_name
- Values: rating_count → Max Sort Descending
- Insight: Identify popular products.

**7. How many products have a discount of 50% or more?**
- Method:
Added a calculated column:
=COUNTIF(F:F,  ">=50%")
- Insight: Know how many heavily discounted products exist.

**8. What is the distribution of product ratings?**
- Rows: rating
- Values: product_name → Count
- Insight: See how ratings are spread (e.g., how many 3.0, 4.5, 5.0)

**9. What is the total potential revenue by category?**
- Calculated Column: = actual_price * rating_count
- Rows: category
- Values: new column → Sum
- Insight: Estimate revenue potential by category.

**10. Number of unique products per price range bucket**
- Added a column for price bucket:
=IF(actual_price<200,"<₹200",IF(actual_price<=500,"₹200–₹500",">₹500"))
- Rows: new bucket column
- Values: product_name → Count 
- Insight: Segment product pricing.

**11. How does the rating relate to the level of discount?**
- Insert a Scatter Plot:
- Select: rating and discount_percentage
- Insert → Chart → Scatter Plot
Insight: Look for any visible trend (e.g., higher ratings = less discount?).

**12. How many products have fewer than 1,000 reviews?**
- Calculated Column:
=COUNTIF(H:H, “<1000”)
- Insight: Know how many low-engagement products exist.

**13. Which categories have products with the highest discounts?**
- Rows: category
- Values: discount_percentage → Max
- Sort Descending
- Insight: Discover which categories offer the biggest discounts.

**14. Top 5 products by rating and number of reviews combined**
- Calculated Column: = rating + rating_count
- Then: Pivot Table with product name
- Values: New column → Max
- Sort descending → Show Top 5
- Insight: Find star products.

#

## KPIs Displayed on Dashboard
- Avg Discount	Average discount across all products
- Total Products	Total products analyzed
- Products with 50% or more discount
- Products with less than 1000 reviews

#

[Dashboard Overview](https://docs.google.com/spreadsheets/d/1cBnwltwFj1-qkFwa-j96SrahNILo2Hmg/edit?usp=drivesdk&ouid=113761501311242743522&rtpof=true&sd=true) 

#

## Insights Summary
- Categories like Home Improvement and Health & Personal care offer the highest discounts
- Products in Electronics category get the most reviews.
- High-rated products don’t always need high discounts.
- Majority of products fall in the >₹500 price range.
- Customer engagement varies strongly across categories.

#

## Recommendations & Reasoning
1. Promote top-rated products with more reviews  
Why: Electronics have high engagement. Promoting these trusted, high-rated products can increase visibility and sales without needing extra discounts.

2. Improve engagement for low-review products with potential  
Why: Some high-quality products may lack attention. Boosting them with better visibility or review incentives can increase customer interaction.

3. Optimize pricing for low-revenue categories  
Why: If some higher-priced categories earn low revenue, testing price adjustments or bundles may make them more appealing and competitive.

4. Highlight high-discount categories during marketing campaigns  
Why: Categories already offering strong discounts (like Home Improvement) are perfect for promotions. Featuring them can attract deal-focused buyers and boost sales.

