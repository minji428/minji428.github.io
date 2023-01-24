---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Combine Two Tables
author: Ms. Park's Workshop
title: Combine Two Tables
category: SQL
tags: [sql, LeetCode]
date: 2023-01-24 16:03:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/combine-two-tables/">Combine Two Tables</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/175-1.jpg" title="175-1.jpg" alt="175-1.jpg"/><br>
<img src="/assets/img/posts/sql/175-2.jpg" title="175-2.jpg" alt="175-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT firstName, lastName, city, state
FROM PERSON
    LEFT JOIN ADDRESS ON PERSON.PERSONID = ADDRESS.PERSONID
```
<h2>수행 결과</h2>
<img src="/assets/img/posts/sql/175result.jpg" title="175result.jpg" alt="175result.jpg"/><br>