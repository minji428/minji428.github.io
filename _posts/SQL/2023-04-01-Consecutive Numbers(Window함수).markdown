---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Consecutive Numbers(Window함수)
author: Ms. Park's Workshop
title: Consecutive Numbers(Window함수)
category: SQL
tags: [sql, LeetCode]
date: 2023-04-01 22:26:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/consecutive-numbers/">Consecutive Numbers</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/180-1.jpg" title="180-1.jpg" alt="180-1.jpg"/><br>
<img src="/assets/img/posts/sql/180-2.jpg" title="180-2.jpg" alt="180-2.jpg"/><br>

<h2>코드</h2>
<h3>Window함수 사용</h3>
<h3>MS SQL Server/Oracle</h3>

```sql
SELECT DISTINCT L.NUM AS ConsecutiveNums
FROM (
     SELECT NUM
          , LEAD(NUM, 1) OVER (ORDER BY ID) AS NEXT
          , LEAD(NUM, 2) OVER (ORDER BY ID) AS AFTERNEXT
     FROM LOGS
) L
WHERE L.NUM = L.NEXT AND L.NUM = L.AFTERNEXT
```


<h3>Window함수 미사용</h3>
<h3>Oracle</h3>

```sql
SELECT DISTINCT L.NUM AS ConsecutiveNums
FROM LOGS L
    INNER JOIN LOGS F ON L.ID + 1 = F.ID
    INNER JOIN LOGS S ON L.ID + 2 = S.ID
WHERE L.NUM = F.NUM 
    AND L.NUM = S.NUM
```


<h2>수행결과</h2>
<img src="/assets/img/posts/sql/180result.jpg" title="180result.jpg" alt="180result.jpg"/><br>
<img src="/assets/img/posts/sql/180result1.jpg" title="180result1.jpg" alt="180result1.jpg"/><br>