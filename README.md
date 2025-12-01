# MSCS 634 Lab 6: Association Rule Mining

## Overview
This lab explores **association rule mining** using the **Apriori** and **FP-Growth** algorithms. The goal is to analyze transactional data, identify frequent itemsets, generate meaningful association rules, and visualize insights using Seaborn. This lab demonstrates how data mining techniques can uncover hidden patterns in retail datasets.

## Dataset
The analysis uses the **Online Retail Dataset** (UCI Machine Learning Repository). The dataset contains transactional records with:

- `InvoiceNo` – Unique transaction ID  
- `StockCode` – Product identifier  
- `Description` – Product description  
- `Quantity` – Number of items purchased  
- `CustomerID` – Unique customer ID  
- `InvoiceDate` – Transaction date  
- `UnitPrice` – Price per item  

The dataset was cleaned to remove missing `CustomerID` values and canceled transactions (`Quantity <= 0`) before analysis.

## Key Steps
1. **Data Preparation**
   - Loaded and explored the dataset.  
   - Cleaned missing and invalid data.  
   - Created a transaction basket for item-level analysis.  
   - Visualized the most frequent items and item co-occurrence using Seaborn.

2. **Frequent Itemset Mining**
   - Used **Apriori** and **FP-Growth** algorithms with a minimum support threshold of 0.01.  
   - Extracted frequent itemsets and compared the top itemsets.  
   - Visualized top itemsets with bar plots.

3. **Association Rule Generation**
   - Generated rules with a minimum confidence of 0.5.  
   - Calculated metrics: **support**, **confidence**, and **lift**.  
   - Visualized rules using scatter plots of confidence vs. support and lift.

4. **Comparative Analysis**
   - Compared **Apriori** vs **FP-Growth** in terms of runtime efficiency and frequent itemsets generated.  
   - Discussed challenges and observations regarding parameter tuning, data cleaning, and interpretation of rules.

## Key Insights
- Top purchased items include [list a few examples from your dataset].  
- Strong associations found include rules such as “customers who buy [Item A] also buy [Item B]”.  
- FP-Growth was more efficient than Apriori, especially for larger datasets, due to avoidance of candidate generation.  
- Visualizations helped identify high-support and high-lift rules, revealing actionable patterns for marketing and inventory decisions.

## Challenges and Decisions
- Cleaning item descriptions to remove duplicates and special characters.  
- Selecting appropriate **support** and **confidence** thresholds to balance number of rules and meaningful insights.  
- Handling sparse transactional data to ensure algorithms ran efficiently.  

## Repository Structure
