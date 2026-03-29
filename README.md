# Lab 6: Association Rule Mining with Apriori and FP-Growth

## Purpose of the Lab
The purpose of this lab is to explore transactional retail data and identify patterns in customer purchasing behavior using frequent itemset mining. The lab applies two popular algorithms, Apriori and FP-Growth, to discover frequently co-purchased items and generate association rules. These insights can help businesses make data-driven decisions for product placement, promotions, and recommendations.

---

## Key Insights
- **Top-selling items** - Certain products, such as candles, gift items, and decorative products, appear more frequently across transactions.
- **Item associations** - Items frequently purchased together were identified, e.g., heart-themed decorative items often co-occur in transactions.
- **Strong association rules** - High-confidence rules revealed patterns such as “customers who bought Item A are likely to also buy Item B,” with lift values greater than 1 indicating strong associations.
- **Algorithm performance** - FP-Growth was faster and more memory-efficient than Apriori on this dataset, while both produced similar frequent itemsets with the same support threshold. 

---

## Challenges & Decisions
**1. Data Cleaning**
- Some transactions were canceled, and there were missing product descriptions.
- **Decision:** Removed canceled orders and rows with missing descriptions to ensure accurate analysis.
**2. Transaction Format Conversion**
- Apriori and FP-Growth require a one-hot encoded transaction matrix.
- **Decision:** Used TransactionEncoder to convert the dataset into the required format.
**3. Support Threshold Selection**
- Low support thresholds increase computation time and memory usage.
- **Decision:** Tested different thresholds and selected a minimum support of 0.02 to balance result significance and efficiency.
**4. Algorithm Choice**
- Apriori generates candidate sets and can be slow for large datasets.
- **Decision:** Compared Apriori with FP-Growth and observed that FP-Growth is faster and more scalable for large datasets.

---

## Conclusion
This lab demonstrated how to use Apriori and FP-Growth to perform market basket analysis on real-world retail data. By generating frequent itemsets and association rules, we identified patterns in customer purchasing behavior, which can guide business strategies such as product bundling, promotions, and targeted marketing. The FP-Growth algorithm proved to be more efficient for large datasets, while both algorithms produced comparable results in terms of the frequent itemsets discovered.

Overall, the lab highlights the importance of data preparation, algorithm selection, and interpretation of association rules in extracting actionable insights from transactional data.
