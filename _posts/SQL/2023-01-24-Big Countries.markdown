---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Big Countries
author: Ms. Park's Workshop
title: Big Countries
category: SQL
tags: [sql, LeetCode]
date: 2023-01-24 15:51:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/big-countries/">Big Countries</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/595-1.jpg" title="595-1.jpg" alt="595-1.jpg"/><br>
<img src="/assets/img/posts/sql/595-2.jpg" title="595-2.jpg" alt="595-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT name, population, area
FROM WORLD
WHERE AREA > 3000000
    OR POPULATION >= 25000000
```

<h2>수행 결과</h2>
<img src="/assets/img/posts/sql/595result.jpg" title="595result.jpg" alt="595result.jpg"/><br>
