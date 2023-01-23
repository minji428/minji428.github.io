---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Rising Temperature
author: Ms. Park's Workshop
title: Rising Temperature
category: SQL
tags: [sql, LeetCode]
date: 2023-01-22 21:36:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/rising-temperature/">Rising Temperature</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/197-1.jpg" title="197-1.jpg" alt="197-1.jpg"/><br>
<img src="/assets/img/posts/sql/197-2.jpg" title="197-2.jpg" alt="197-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT TODAY.ID AS id
FROM WEATHER TODAY
    INNER JOIN WEATHER YESTERDAY ON YESTERDAY.RECORDDATE + (INTERVAL '1' DAY) = TODAY.RECORDDATE
WHERE TODAY.TEMPERATURE > YESTERDAY.TEMPERATURE
```

<h3>MYSQL</h3>

```sql
SELECT TODAY.ID AS id
FROM WEATHER AS TODAY
    INNER JOIN WEATHER AS YESTERDAY ON DATE_ADD(YESTERDAY.RECORDDATE, INTERVAL 1 DAY) = TODAY.RECORDDATE
WHERE TODAY.TEMPERATURE > YESTERDAY.TEMPERATURE
```

<h2>수행 결과</h2>
<img src="/assets/img/posts/sql/197result.jpg" title="197result.jpg" alt="197result.jpg"/><br>

<h2>참고사항</h2>
<h3>Oracle 시간 더하기, 빼기</h3>
* INTERVAL
    + SYSDATE + (INTERVAL '1' YEAR)     --1년 더하기
    + SYSDATE + (INTERVAL '1' MONTH)   --1개월 더하기
    + SYSDATE + (INTERVAL '1' DAY)     --1일 더하기
    + SYSDATE + (INTERVAL '1' HOUR)    --1시간 더하기 
    + SYSDATE + (INTERVAL '1' MINUTE)  --1분 더하기
    + SYSDATE + (INTERVAL '1' SECOND)  --1초 더하기
    + SYSDATE + (INTERVAL '02:10' HOUR TO MINUTE)   --2시간10분 더하기
    + SYSDATE + (INTERVAL '01:30' MINUTE TO SECOND) --1분30초 더하기

<h3>MYSQL 시간 더하기, 빼기</h3>
* DATE_ADD(기준날짜, INTERVAL)
    + SELECT DATE_ADD(NOW(), INTERVAL 1 SECOND)
    + SELECT DATE_ADD(NOW(), INTERVAL 1 MINUTE)
    + SELECT DATE_ADD(NOW(), INTERVAL 1 HOUR)
    + SELECT DATE_ADD(NOW(), INTERVAL 1 DAY)
    + SELECT DATE_ADD(NOW(), INTERVAL 1 MONTH)
    + SELECT DATE_ADD(NOW(), INTERVAL 1 YEAR)
    + SELECT DATE_ADD(NOW(), INTERVAL -1 YEAR)
* DATE_SUB(기준날짜, INTERVAL)
    + SELECT DATE_SUB(NOW(), INTERVAL 1 SECOND)


