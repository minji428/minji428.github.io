---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Observation Station 18
author: Ms. Park's Workshop
title: Weather Observation Station 18
category: SQL
tags: [sql, HackerRank]
date: 2023-01-29 19:46:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-18/problem">Weather Observation Station 18</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_18.jpg" title="Weather_Observation_Station_18.jpg" alt="Weather_Observation_Station_18.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT ROUND(ABS(MIN(LAT_N)-MAX(LAT_N)) + ABS(MIN(LONG_W)-MAX(LONG_W)), 4)
FROM STATION;
```
