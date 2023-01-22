---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Customers Who Never Order
author: Ms. Park's Workshop
title: Customers Who Never Order
category: SQL
tags: [sql, LeetCode]
date: 2023-01-22 21:07:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/customers-who-never-order/">Customers Who Never Order</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/183-1.jpg" title="183-1.jpg" alt="183-1.jpg"/><br>
<img src="/assets/img/posts/sql/183-2.jpg" title="183-2.jpg" alt="183-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT CUSTOMERS.NAME AS Customers
FROM CUSTOMERS
    LEFT JOIN ORDERS ON CUSTOMERS.ID = ORDERS.CUSTOMERID
WHERE ORDERS.ID IS NULL
```