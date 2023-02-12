---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Population Density Difference
author: Ms. Park's Workshop
title: Population Density Difference
category: SQL
tags: [sql, HackerRank]
date: 2023-02-12 17:39:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/population-density-difference/problem">Population Density Difference</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Population_Density_Difference.jpg" title="Population_Density_Difference.jpg" alt="Population_Density_Difference.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT MAX(POPULATION) - MIN(POPULATION)
FROM CITY
```
