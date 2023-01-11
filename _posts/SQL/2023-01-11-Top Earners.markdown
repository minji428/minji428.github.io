---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Top Earners
author: Ms. Park's Workshop
title: Top Earners
category: SQL
tags: [sql, HackerRank]
date: 2023-01-11 19:49:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/earnings-of-employees/problem?h_r=internal-search">Top Earners</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Top_Earners1.jpg" title="Top_Earners1.jpg" alt="Top_Earners1.jpg"/><br>
<img src="/assets/img/posts/sql/Top_Earners2.jpg" title="Top_Earners2.jpg" alt="Top_Earners2.jpg"/><br>
<img src="/assets/img/posts/sql/Top_Earners3.jpg" title="Top_Earners3.jpg" alt="Top_Earners3.jpg"/><br>

<h2>코드</h2>
<h3>MySQL</h3>

```sql
SELECT salary * months AS earnings
     , count(*)
FROM employee
GROUP BY earnings
ORDER BY earnings DESC
LIMIT 1
```