---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Placements
author: Ms. Park's Workshop
title: Placements
category: SQL
tags: [sql, HackerRank]
date: 2023-02-17 21:55:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/placements/problem">Placements</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Placements1.jpg" title="Placements1.jpg" alt="Placements1.jpg"/><br>
<img src="/assets/img/posts/sql/Placements2.jpg" title="Placements2.jpg" alt="Placements2.jpg"/><br>
<img src="/assets/img/posts/sql/Placements3.jpg" title="Placements3.jpg" alt="Placements3.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT S.NAME
FROM FRIENDS F
    INNER JOIN STUDENTS S ON F.ID = S.ID
    INNER JOIN PACKAGES MS ON MS.ID = F.ID
    INNER JOIN PACKAGES PS ON PS.ID = F.FRIEND_ID
WHERE MS.SALARY < PS.SALARY
ORDER BY PS.SALARY ASC
```

<h2>참고사항</h2>
가장 친한 친구가 자신보다 더 높은 급여를 제안받은 학생의 이름을 출력하는 쿼리를 작성 <br/>
이름은 가장 친한 친구에게 제공되는 급여 금액 순으로 정렬 <br/>
두 명의 학생이 동일한 급여 제안을 받지 않았음 <br/>