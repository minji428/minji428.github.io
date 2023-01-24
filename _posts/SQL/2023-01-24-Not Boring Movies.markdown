---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Not Boring Movies
author: Ms. Park's Workshop
title: Not Boring Movies
category: SQL
tags: [sql, LeetCode]
date: 2023-01-24 15:34:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/not-boring-movies/">Not Boring Movies</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/620-1.jpg" title="620-1.jpg" alt="620-1.jpg"/><br>
<img src="/assets/img/posts/sql/620-2.jpg" title="620-2.jpg" alt="620-2.jpg"/><br>

<h2>코드</h2>
<h3>MYSQL</h3>

```sql
SELECT id, movie, description, rating
FROM Cinema
WHERE MOD(ID, 2) = 1 
    AND description != "boring"
ORDER BY rating DESC
```
<h2>수행 결과</h2>
<img src="/assets/img/posts/sql/620result.jpg" title="620result.jpg" alt="620result.jpg"/><br>
