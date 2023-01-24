---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Duplicate Emails
author: Ms. Park's Workshop
title: Duplicate Emails
category: SQL
tags: [sql, LeetCode]
date: 2023-01-24 15:59:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/duplicate-emails/">Duplicate Emails</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/182-1.jpg" title="182-1.jpg" alt="182-1.jpg"/><br>
<img src="/assets/img/posts/sql/182-2.jpg" title="182-2.jpg" alt="182-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT Email
FROM PERSON
GROUP BY EMAIL
HAVING COUNT(ID) >= 2
```
<h2>수행 결과</h2>
<img src="/assets/img/posts/sql/182result.jpg" title="182result.jpg" alt="182result.jpg"/><br>