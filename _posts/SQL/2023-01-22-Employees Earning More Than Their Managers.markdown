---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Employees Earning More Than Their Managers
author: Ms. Park's Workshop
title: Employees Earning More Than Their Managers
category: SQL
tags: [sql, LeetCode]
date: 2023-01-22 21:22:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/employees-earning-more-than-their-managers/">Employees Earning More Than Their Managers</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/181-1.jpg" title="181-1.jpg" alt="181-1.jpg"/><br>
<img src="/assets/img/posts/sql/181-2.jpg" title="182-2.jpg" alt="182-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT EMPLOYEE.NAME AS Employee
FROM EMPLOYEE
    INNER JOIN EMPLOYEE AS MANAGER ON EMPLOYEE.MANAGERID = MANAGER.ID
WHERE EMPLOYEE.SALARY > MANAGER.SALARY
```