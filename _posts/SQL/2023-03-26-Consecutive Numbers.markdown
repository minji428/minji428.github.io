---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Consecutive Numbers
author: Ms. Park's Workshop
title: Consecutive Numbers
category: SQL
tags: [sql, LeetCode]
date: 2023-03-26 20:40:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/consecutive-numbers/">Consecutive Numbers</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/180-1.jpg" title="180-1.jpg" alt="180-1.jpg"/><br>
<img src="/assets/img/posts/sql/180-2.jpg" title="180-2.jpg" alt="180-2.jpg"/><br>

<h2>코드</h2>
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