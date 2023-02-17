---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Observation Station 3
author: Ms. Park's Workshop
title: Weather Observation Station 3
category: SQL
tags: [sql, HackerRank]
date: 2023-02-17 21:10:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-3/problem">Weather Observation Station 3</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_3.jpg" title="Weather_Observation_Station_3.jpg" alt="Weather_Observation_Station_3.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE MOD(ID, 2) = 0
```

<h2>참고사항</h2>
id가 짝수인거 출력하기 <br/>
MOD(n,m) -> m을 n으로 나누었을 때 나머지를 반환<br/>
