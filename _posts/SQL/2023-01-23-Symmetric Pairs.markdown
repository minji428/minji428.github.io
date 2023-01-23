---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Symmetric Pairs
author: Ms. Park's Workshop
title: Symmetric Pairs
category: SQL
tags: [sql, HackerRank]
date: 2023-01-23 22:59:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/symmetric-pairs/problem?h_r=internal-search">Symmetric Pairs</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Symmetric_pairs.jpg" title="Symmetric_pairs.jpg" alt="Symmetric_pairs.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT X, Y
FROM FUNCTIONS
WHERE X = Y 
GROUP BY X, Y
HAVING COUNT(*) = 2
UNION
SELECT A.X, A.Y
FROM FUNCTIONS A
    INNER JOIN FUNCTIONS B ON A.X = B.Y AND A.Y = B.X
WHERE A.X < A.Y
ORDER BY X;
```

<h3>MYSQL</h3>

```sql
SELECT X, Y
FROM FUNCTIONS
WHERE X = Y 
GROUP BY X, Y
HAVING COUNT(*) = 2

UNION 

SELECT A.X, A.Y
FROM FUNCTIONS AS A
    INNER JOIN FUNCTIONS AS B ON A.X = B.Y AND A.Y = B.X
WHERE A.X < A.Y
ORDER BY X
```

<h2>참고사항</h2>

UNION이 있을 때 ORDER BY는 맨 마지막에 사용<br/>
중간 쿼리문에서는 사용할 수 없음<br/>
마지막에 사용하게 되면 전체 쿼리에 대해서 ORDER BY를 진행하게 됨