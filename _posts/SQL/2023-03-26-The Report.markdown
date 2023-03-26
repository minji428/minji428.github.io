---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: The Report
author: Ms. Park's Workshop
title: The Report
category: SQL
tags: [sql, HackerRank]
date: 2023-03-26 19:46:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/the-report/problem?h_r=internal-search">The Report</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/The_Report1.jpg" title="The_Report1.jpg" alt="The_Report1.jpg"/><br>
<img src="/assets/img/posts/sql/The_Report2.jpg" title="The_Report2.jpg" alt="The_Report2.jpg"/><br>
<img src="/assets/img/posts/sql/The_Report3.jpg" title="The_Report3.jpg" alt="The_Report3.jpg"/><br>
<img src="/assets/img/posts/sql/The_Report4.jpg" title="The_Report4.jpg" alt="The_Report4.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT CASE WHEN G.GRADE < 8 THEN NULL ELSE S.NAME
    , G.GRADE
    , S.MARKS
FROM STUDENTS S
    INNER JOIN GRADES G ON S.MARKS BETWEEN G.MIN_MARK AND G.MAX_MARK
ORDER BY G.GRADE DESC, NAME, S.MARKS;
```
