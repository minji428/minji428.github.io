---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Nth Higthest Salary
author: Ms. Park's Workshop
title: Nth Higthest Salary
category: SQL
tags: [sql, LeetCode]
date: 2023-04-16 16:16:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/nth-highest-salary/">Nth Higthest Salary</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/177-1.jpg" title="177-1.jpg" alt="177-1.jpg"/><br>
<img src="/assets/img/posts/sql/177-2.jpg" title="177-2.jpg" alt="177-2.jpg"/><br>

<h2>코드</h2>
<h3>MySQL</h3>
<h6>CASE WHEN 사용해서 풀기</h6>

```sql
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
  RETURN (
    SELECT CASE WHEN COUNT(SUB.SALARY) < N THEN NULL
                ELSE MIN(SUB.SALARY)
            END
    FROM (
        SELECT DISTINCT SALARY
        FROM EMPLOYEE
        ORDER BY SALARY DESC
        LIMIT N
        ) SUB
  );
END
```
<h6>IF 함수 사용해서 풀기</h6>
<h7>Example</h7>

```sql
// IF (condition, value_if_true, value_if_false)
SELECT IF(500<1000, "YES", "NO")
SELECT IF(500<1000, "YES", NULL)
```

```sql
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
  RETURN (
    SELECT IF(COUNT(SUB.SALARY) < N, NULL, MIN(SUB.SALARY))
    FROM (
        SELECT DISTINCT SALARY
        FROM EMPLOYEE
        ORDER BY SALARY DESC
        LIMIT N
        ) SUB
  );
END
```

<h6>LIMIT OFFSET 사용해서 풀기</h6>

```sql
CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
  SET N = N-1;
  RETURN (
    SELECT DISTINCT SALARY
    FROM EMPLOYEE
    ORDER BY SALARY DESC
    LIMIT 1 OFFSET N
  );
END
```

<h2>수행결과</h2>
<img src="/assets/img/posts/sql/177result.jpg" title="177result.jpg" alt="177result.jpg"/><br>