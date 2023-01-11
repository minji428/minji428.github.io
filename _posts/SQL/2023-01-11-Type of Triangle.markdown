---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Type of Triangle
author: Ms. Park's Workshop
title: Type of Triangle
category: SQL
tags: [sql, HackerRank]
date: 2023-01-11 20:11:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/what-type-of-triangle/problem?h_r=internal-search">Type of Triangle</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Type_of_Triangle1.jpg" title="Type_of_Triangle1.jpg" alt="Type_of_Triangle1.jpg"/><br>
<img src="/assets/img/posts/sql/Type_of_Triangle2.jpg" title="Type_of_Triangle2.jpg" alt="Type_of_Triangle2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT CASE
        WHEN A=B AND B=C THEN 'Equilateral'
        WHEN A+B <= C OR A+C <= B OR B+C <= A THEN 'Not A Triangle'
        WHEN A=B OR B=C OR A=C THEN 'Isosceles'
        ELSE 'Scalene'
       END
FROM Triangles
```