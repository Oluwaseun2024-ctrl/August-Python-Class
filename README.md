# PIZZA SALES PLACE ANALYSIS

An Excel project analyzing a year's worth of sales from a fictitious pizza sales place. The dataset encompasses details such as pizza type, size, quantity, price, and ingredients. The goal is to derive actionable insights to inform strategic decisions and optimize overall operational effectiveness.

### Table of Contents
 - Project Overview
 - Project Scope
 - Project Objectives
 - Expected Outcome
- Document Purpose
- Use Case
- [Data Source](https://github.com/Oluwaseun2024-ctrl/August-Python-Class/blob/main/README.md#data-source)
- Data Cleaning and Processing
- Data Analysis
- Data Visualization
- Recommendation
- Conclusion

### Data Source
The dataset for this project is sourced from [Maven Analytics website](https://app.mavenanalytics.io/datasets?search=pizz) designed specifically for practice purposes. It is presented in an Excel file with four tables (Order Details, Orders, Pizza Types, and Pizzas) comprising 48,620, 21,350, 32, and 96 rows respectively, and 4, 3, 4, and 4 columns respectively. The dataset includes key attributes essential for a comprehensive analysis, such as:


![](https://github.com/Oluwaseun2024-ctrl/August-Python-Class/blob/main/Least%205%20Selling%20Pizzas%20By%20Order.png)

![](https://github.com/Oluwaseun2024-ctrl/August-Python-Class/blob/main/Quarterly%20Sales%20Trend.png)

| Customer No | Customer Name | Customer Age |
|------------ | ------------- | ------------ |
| 1           | Seun          |  99          |
| 2           | Favour        | 106          |

| Company response to consumer      | Resolution Count |
|-----------------------------------|------------------|
| Closed with explanation           | 41,044           |
| Closed with monetary relief       | 14,697           |
| Closed with non-monetary relief   | 5,273            |
| In progress                       | 1,494            |
| Closed                            | 8                |


``` SQL
SELECT
  Company_response_to_consumer,
COUNT
  (Complaint_ID) AS Resolution_Count
From
  Financial_Consumer_Complaints
GROUP BY
  Company_response_to_consumer
ORDER BY
  Resolution_Count DESC
```

```𝐼𝑛𝑣𝑒𝑛𝑡𝑜𝑟𝑦 𝑉𝑎𝑙𝑢𝑒 = 𝑆𝑈𝑀𝑋(′𝐼𝑛𝑣𝑒𝑛𝑡𝑜𝑟𝑦′,𝐼𝑛𝑣𝑒𝑛𝑡𝑜𝑟𝑦[𝑆𝑡𝑜𝑐𝑘𝑂𝑛𝐻𝑎𝑛𝑑]∗ 𝑅𝐸𝐿𝐴𝑇𝐸𝐷(′𝑃𝑟𝑜𝑑𝑢𝑐𝑡′[𝑃𝑟𝑜𝑑𝑢𝑐𝑡𝑃𝑟𝑖𝑐𝑒])) 𝐼𝑛𝑣𝑒𝑛𝑡𝑜𝑟𝑦 𝑉𝑎𝑙𝑢𝑒=$410,241```

``` PYTHON
# Find the most frequent (mode) values for categorical columns
mode_marital_status = data['Marital_Status'].mode()[0] # Mode returns a Series, we select the first value
mode_education = data['Education'].mode()[0]
mode_country = data['Country'].mode()[0]
print("Most common Marital Status: ", mode_marital_status)
print("Most common Education Level: ", mode_education)
print("Most common Country: ", mode_country)
```
