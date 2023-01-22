---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Population Census
author: Ms. Park's Workshop
title: Population Census
category: SQL
tags: [sql, HackerRank]
date: 2023-01-22 20:57:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/asian-population/problem?h_r=internal-search">Population Census</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Population_Census1.jpg" title="Population_Census1.jpg" alt="Population_Census1.jpg"/><br>
<img src="/assets/img/posts/sql/Population_Census2.jpg" title="Population_Census2.jpg" alt="Population_Census2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT SUM(CITY.POPULATION)
FROM CITY
    INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Asia';
```