---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Swap Salary
author: Ms. Park's Workshop
title: Swap Salary
category: SQL
tags: [sql, LeetCode]
date: 2023-02-26 15:04:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://leetcode.com/problems/swap-salary/">Swap Salary</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/627-1.jpg" title="627-1.jpg" alt="627-1.jpg"/><br>
<img src="/assets/img/posts/sql/627-2.jpg" title="627-2.jpg" alt="627-2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
UPDATE SALARY
SET SEX = CASE
            WHEN SEX = 'm' THEN 'f'
          ELSE 'm'
          END
```

<h2>수행결과</h2>
<img src="/assets/img/posts/sql/627result.jpg" title="627result.jpg" alt="627result.jpg"/><br>