---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Department Top Three Salaries(Window함수)
author: Ms. Park's Workshop
title: Department Top Three Salaries(Window함수)
category: SQL
tags: [sql, LeetCode]
date: 2023-04-02 17:38:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/department-top-three-salaries/">Department Top Three Salaries</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/185-1.jpg" title="185-1.jpg" alt="185-1.jpg"/><br>
<img src="/assets/img/posts/sql/185-2.jpg" title="185-2.jpg" alt="185-2.jpg"/><br>
<img src="/assets/img/posts/sql/185-3.jpg" title="185-3.jpg" alt="185-3.jpg"/><br>

<h2>코드</h2>
<h3>Window함수 사용</h3>
<h3>MS SQL Server/Oracle</h3>

```sql
SELECT T.DEPARTMENT
     , T.EMPLOYEE
     , T.SALARY
FROM (
    SELECT DEPARTMENT.NAME AS DEPARTMENT
        , EMPLOYEE.NAME AS EMPLOYEE
        , EMPLOYEE.SALARY
        , DENSE_RANK() OVER (PARTITION BY DEPARTMENTID ORDER BY SALARY DESC) AS DR
    FROM EMPLOYEE
        INNER JOIN DEPARTMENT ON EMPLOYEE.DEPARTMENTID = DEPARTMENT.ID
    ) T
WHERE T.DR <= 3
```


<h2>수행결과</h2>
<img src="/assets/img/posts/sql/185result.jpg" title="185result.jpg" alt="185result.jpg"/><br>