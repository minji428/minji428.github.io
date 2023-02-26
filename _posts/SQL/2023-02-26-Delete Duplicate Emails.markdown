---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Delete Duplicate Emails
author: Ms. Park's Workshop
title: Delete Duplicate Emails
category: SQL
tags: [sql, LeetCode]
date: 2023-02-26 15:41:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/delete-duplicate-emails/">Delete Duplicate Emails</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/196-1.jpg" title="196-1.jpg" alt="196-1.jpg"/><br>
<img src="/assets/img/posts/sql/196-2.jpg" title="196-2.jpg" alt="196-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
 DELETE FROM PERSON
 WHERE ID NOT IN (SELECT MIN(ID)
                    FROM PERSON
                    GROUP BY EMAIL)
```

<h2>수행결과</h2>
<img src="/assets/img/posts/sql/196result.jpg" title="196result.jpg" alt="196result.jpg"/><br>