---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Average Population of Each Continent
author: Ms. Park's Workshop
title: Average Population of Each Continent
category: SQL
tags: [sql, HackerRank]
date: 2023-01-22 21:02:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/what-type-of-triangle/problem?h_r=internal-search">Average Population of Each Continent</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Average_Population_of_Each_Continent1.jpg" title="Average_Population_of_Each_Continent1.jpg" alt="Average_Population_of_Each_Continent1.jpg"/><br>
<img src="/assets/img/posts/sql/Average_Population_of_Each_Continent2.jpg" title="Average_Population_of_Each_Continent2.jpg" alt="Average_Population_of_Each_Continent2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT COUNTRY.CONTINENT 
     , FLOOR(AVG(CITY.POPULATION))
FROM CITY
    INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
GROUP BY COUNTRY.CONTINENT;
```