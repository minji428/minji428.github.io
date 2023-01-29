---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Japan Population
author: Ms. Park's Workshop
title: Japan Population
category: SQL
tags: [sql, HackerRank]
date: 2023-01-29 19:41:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/japan-population/problem">Japan Population</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Japan_Population.jpg" title="Japan_Population.jpg" alt="Japan_Population.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT SUM(POPULATION)
FROM CITY
WHERE COUNTRYCODE= 'JPN';
```
