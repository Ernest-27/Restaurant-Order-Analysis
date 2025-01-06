# Restaurant-Order-Analysis

### Project Overview

This repository contains SQL scripts designed for creating and analyzing a sample database schema, focusing on menu items and order details. It aims to provide insights into the order/sales performance of a restaurant over a two months span. This analysis helps spot trends, make recommendations and feedback to the owners/stakeholders.

### Data Sources

Restaurant Orders:  The primary file used for this analysis is the SQL file, containing datailed information about the menu in the store and the orders that were processed.

### Tools

- SQL workbench - Data analysis

### Data Cleaning & Preparation

This dataset used in this project was found to be clean and structured. No extra data cleaning was needed.

### Exploratory Data Analysis

- What is the total number of menu items?
- What is the most expensive item?
- What as the top-seller item on the menu and the category it belonged to?
- What is the total category of meals available and the most profitable category?
- What is the average price of each category of meals?
- What is the total number of order placed?
- What was the busiest date? What was the busiest day of the week in general? What was the busiest hour?
- What was the total price?

### Data Analysis

```sql
create view table_view as 
select * from order_details
left join menu_items
on order_details.item_id = menu_items.menu_item_id;
```

### Summary of the Results/Findings

- The best performing meal was Shrimp Scampi and it belonged in the Italian category.
- The total number of menu items is 32.
- Total number of orders is 5370.
- The busiest day of the week are Mondays, the busiest date was Febuary 1st 2023, the busiest hour was within 12-1pm.

### Recommendations

- Keep the Italian menu and ensure the customers that like Italian meals are retained.
- The Shrimp Scampi is the most desired menu, so it should always be available.
- Ensure we do not have staff shortage on Mondays, as that is the most productive day.
