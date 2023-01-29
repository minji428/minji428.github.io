---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Observation Station 2
author: Ms. Park's Workshop
title: Weather Observation Station 2
category: SQL
tags: [sql, HackerRank]
date: 2023-01-29 19:43:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-2/problem">Weather Observation Station 2</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_2.jpg" title="Weather_Observation_Station_2.jpg" alt="Weather_Observation_Station_2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT ROUND(SUM(LAT_N), 2)
     , ROUND(SUM(LONG_W), 2)
FROM STATION
```
