---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Observation Station 13
author: Ms. Park's Workshop
title: Weather Observation Station 13
category: SQL
tags: [sql, HackerRank]
date: 2023-02-12 18:46:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-13/problem">Weather Observation Station 13</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_13.jpg" title="Weather_Observation_Station_13.jpg" alt="Weather_Observation_Station_13.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT TRUNC(SUM(LAT_N), 4)
FROM STATION
WHERE LAT_N > 38.7880
    AND LAT_N < 137.2345
```
```sql
SELECT TRUNC(SUM(LAT_N), 4)
FROM STATION
WHERE LAT_N BETWEEN 38.7880 AND 137.2345
```