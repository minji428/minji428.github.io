---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Ovservation Station 9
author: Ms. Park's Workshop
title: Weather Ovservation Station 9
category: SQL
tags: [sql, LeetCode]
date: 2023-04-09 14:34:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-9/problem?h_r=internal-search">Weather Ovservation Station 9</a>
<!-- outline-end -->
<a href="https://regexone.com/lesson/introduction_abcs">정규표현식 튜토리얼</a>
<a href="https://regexr.com/">정규표현식 테스트 해볼 수 있는 사이트</a>

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_9.jpg" title="Weather_Observation_Station_9.jpg" alt="Weather_Observation_Station_9.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE REGEXP_LIKE (CITY, '^[aeiou].*[aeiou]$', 'i')
;
```
<h3>MySQL</h3>

```sql
SELECT DISTINCT CITY
FROM STATION
WHERE CITY REGEXP '^[aeiou].*[aeiou]$'
```