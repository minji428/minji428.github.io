---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Reformat Department Table
author: Ms. Park's Workshop
title: Reformat Department Table
category: SQL
tags: [sql, LeetCode]
date: 2023-01-11 21:24:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/reformat-department-table/">1179. Reformat Department Table</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/1179-1.jpg" title="1179-1.jpg" alt="1179-1.jpg"/><br>
<img src="/assets/img/posts/sql/1179-2.jpg" title="1179-2.jpg" alt="1179-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT id, SUM(CASE WHEN month = 'Jan' THEN revenue ELSE NULL END) AS Jan_Revenue
         , SUM(CASE WHEN month = 'Feb' THEN revenue ELSE NULL END) AS Feb_Revenue
         , SUM(CASE WHEN month = 'Mar' THEN revenue ELSE NULL END) AS Mar_Revenue
         , SUM(CASE WHEN month = 'Apr' THEN revenue ELSE NULL END) AS Apr_Revenue
         , SUM(CASE WHEN month = 'May' THEN revenue ELSE NULL END) AS May_Revenue
         , SUM(CASE WHEN month = 'Jun' THEN revenue ELSE NULL END) AS Jun_Revenue
         , SUM(CASE WHEN month = 'Jul' THEN revenue ELSE NULL END) AS Jul_Revenue
         , SUM(CASE WHEN month = 'Aug' THEN revenue ELSE NULL END) AS Aug_Revenue
         , SUM(CASE WHEN month = 'Sep' THEN revenue ELSE NULL END) AS Sep_Revenue
         , SUM(CASE WHEN month = 'Oct' THEN revenue ELSE NULL END) AS Oct_Revenue
         , SUM(CASE WHEN month = 'Nov' THEN revenue ELSE NULL END) AS Nov_Revenue
         , SUM(CASE WHEN month = 'Dec' THEN revenue ELSE NULL END) AS Dec_Revenue
FROM department
GROUP BY id
```