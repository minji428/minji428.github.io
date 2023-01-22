---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: African Cities
author: Ms. Park's Workshop
title: African Cities
category: SQL
tags: [sql, HackerRank]
date: 2023-01-22 20:46:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/african-cities/problem?h_r=internal-search">African Cities</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/African_Cities1.jpg" title="African_Cities1.jpg" alt="African_Cities1.jpg"/><br>
<img src="/assets/img/posts/sql/African_Cities2.jpg" title="African_Cities2.jpg" alt="African_Cities2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT CITY.NAME
FROM CITY
    INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Africa';
```

<h2>참고사항</h2>
INNER JOIN은 둘 다 결과 값이 있을 때 <br/>
LEFT JOIN 은 왼쪽 테이블에 결과 값이 있을 경우 다 출력 <br/>
