---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Weather Observation Station 19
author: Ms. Park's Workshop
title: Weather Observation Station 19
category: SQL
tags: [sql, HackerRank]
date: 2023-02-17 21:42:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/weather-observation-station-19/problem">Weather Observation Station 19</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Weather_Observation_Station_19.jpg" title="Weather_Observation_Station_19.jpg" alt="Weather_Observation_Station_19.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT ROUND(SQRT(POWER(MIN(LAT_N) - MAX(LAT_n),2) + POWER(MIN(LONG_W) - MAX(LONG_W), 2)) ,4)
FROM STATION
```

<h2>참고사항</h2>
두가지 점 사이의 거리를 구하는 문제
<a href="https://en.wikipedia.org/wiki/Euclidean_distance">Euclidean Distance</a>
<img src="/assets/img/posts/sql/Weather_Observation_Station_19_1.jpg" title="Weather_Observation_Station_19_1.jpg" alt="Weather_Observation_Station_19_1.jpg"/><br>
<table>
    <thead>
        <tr>
            <th>함수</th>
            <th>설명</th>
            <th>예시</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>제곱</td>
            <td>POWER(n1, n2)</td>
            <td>POWER(5, 2) -> 25</td>
        </tr>
        <tr>
            <td>제곱근</td>
            <td>SQRT(대상숫자)</td>
            <td>SQRT(9) -> 3</td>
        </tr>
        <tr>
            <td>소수점 반올림</td>
            <td>ROUND(n1, n2)</td>
            <td>ROUND(12.456, 2) -> 12.46</td>
        </tr>
    </tbody>
</table>
