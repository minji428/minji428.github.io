---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Department Highest Salary(Window함수)
author: Ms. Park's Workshop
title: Department Highest Salary(Window함수)
category: SQL
tags: [sql, LeetCode]
date: 2023-04-02 17:30:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/department-highest-salary/">Department Highest Salary</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/184-1.jpg" title="184-1.jpg" alt="184-1.jpg"/><br>
<img src="/assets/img/posts/sql/184-2.jpg" title="184-2.jpg" alt="184-2.jpg"/><br>
<img src="/assets/img/posts/sql/184-3.jpg" title="184-3.jpg" alt="184-3.jpg"/><br>

<h2>코드</h2>
<h3>Window함수 사용</h3>
<h3>MS SQL Server/Oracle</h3>

```sql
SELECT MS.DEPARTMENT
     , MS.NAME AS EMPLOYEE
     , MS.SALARY
FROM (
     SELECT EMPLOYEE.NAME
          , EMPLOYEE.SALARY
          , DEPARTMENT.NAME AS DEPARTMENT
          , MAX(SALARY) OVER (PARTITION BY DEPARTMENTID) MAX_SALARY
     FROM EMPLOYEE
     INNER JOIN DEPARTMENT ON EMPLOYEE.DEPARTMENTID = DEPARTMENT.ID
     ) MS
WHERE MS.SALARY = MS.MAX_SALARY
```


<h3>Window함수 미사용</h3>
<h3>Oracle</h3>

```sql
SELECT D.NAME AS DEPARTMENT
     , E.NAME AS EMPLOYEE
     , E.SALARY
FROM EMPLOYEE E
    INNER JOIN (
        SELECT DEPARTMENTID
             , MAX(SALARY) AS MAX_SALARY
        FROM EMPLOYEE
        GROUP BY DEPARTMENTID
    ) DH ON E.DEPARTMENTID = DH.DEPARTMENTID
          AND E.SALARY = DH.MAX_SALARY
     INNER JOIN DEPARTMENT D ON D.ID = E.DEPARTMENTID;
```


<h2>수행결과</h2>
<img src="/assets/img/posts/sql/184result.jpg" title="184result.jpg" alt="184result.jpg"/><br>