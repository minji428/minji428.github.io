---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Observation Station 11
author: Ms. Park's Workshop
title: Weather Observation Station 11
category: SQL
tags: [sql, HackerRank]
date: 2023-02-12 18:36:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-11/problem">Weather Observation Station 11</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_11.jpg" title="Weather_Observation_Station_11.jpg" alt="Weather_Observation_Station_11.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE SUBSTR(CITY, 1, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
    OR SUBSTR(CITY, -1, 2) NOT IN ('a', 'e', 'i', 'o', 'u')
```

<h2>참고사항</h2>
Oracle 에는 left, right가 없음<br/>
substr로 문자열을 잘라서 비교해야함<br/>
위의 방법 말고 정규식으로 찾는 방법도 있음<br/>
혹은 NOT LIKE 로 하기
