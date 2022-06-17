# 8-Week-SQL-Challenge

<h2>Case_Study #1 : Dannys_diner <a href="https://8weeksqlchallenge.com/case-study-1/"><img src="https://camo.githubusercontent.com/53418bbd5a503cda20064610bd03cbbee3b0d1c06fea42a752ed4a73f95f3d5b/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f566965772d536f6c7574696f6e5f436173655f53747564795f312d3937313930313f7374796c653d666f722d7468652d6261646765266c6f676f3d474954485542" alt="View Data Exploration Folder" data-canonical-src="https://img.shields.io/badge/View-Solution_Case_Study_1-971901?style=for-the-badge&amp;logo=GITHUB" style="max-width: 100%;"></a><h2>

  
1. What is the total amount each customer spent at the restaurant?

```SQL
select s.customer_id,sum(m.price) as total_Amt_spent from dannys_diner.sales s
join dannys_diner.menu m
on (s.product_id=m.product_id)
group by customer_id;
order by customer_id;
```

| customer_id | total_amt_spent |
| ----------- | --------------- |
| A           | 76              |
| B           | 74              |
| C           | 36              |

---
  
2. How many days has each customer visited the restaurant?

  ```SQL  
  select customer_id,count(distinct order_date) as Number_of_Days
  from dannys_diner.sales
  group by customer_id;
  ```
  | customer_id | number_of_days |
  | ----------- | -------------- |
  | A           | 4              |
  | B           | 6              |
  | C           | 2              |
 ---  
  
3. What was the first item from the menu purchased by each customer?

4. What is the most purchased item on the menu and how many times was it purchased by all customers?

5. Which item was the most popular for each customer?

6. Which item was purchased first by the customer after they became a member?

7. Which item was purchased just before the customer became a member?

8. What is the total items and amount spent for each member before they became a member?

9.  If each $1 spent equates to 10 points and sushi has a 2x points multiplier - how many points would each customer have?

10. In the first week after a customer joins the program (including their join date) they earn 2x points on all items, not just sushi - how many points do customer A and B have at the end of January?
