---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Top Competitors
author: Ms. Park's Workshop
title: Top Competitors
category: SQL
tags: [sql, HackerRank]
date: 2023-02-12 19:11:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/full-score/problem">Top Competitors</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Top_Competitors1.jpg" title="Top_Competitors1.jpg" alt="Top_Competitors1.jpg"/><br>
<img src="/assets/img/posts/sql/Top_Competitors2.jpg" title="Top_Competitors2.jpg" alt="Top_Competitors2.jpg"/><br>
<img src="/assets/img/posts/sql/Top_Competitors3.jpg" title="Top_Competitors3.jpg" alt="Top_Competitors3.jpg"/><br>
<img src="/assets/img/posts/sql/Top_Competitors4.jpg" title="Top_Competitors4.jpg" alt="Top_Competitors4.jpg"/><br>
<img src="/assets/img/posts/sql/Top_Competitors5.jpg" title="Top_Competitors5.jpg" alt="Top_Competitors5.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT H.HACKER_ID
     , H.NAME
FROM SUBMISSIONS S
        INNER JOIN HACKERS H ON S.HACKER_ID = H.HACKER_ID
        INNER JOIN CHALLENGES C ON S.CHALLENGE_ID = C.CHALLENGE_ID
        INNER JOIN DIFFICULTY D ON C.DIFFICULTY_LEVEL = D.DIFFICULTY_LEVEL
WHERE S.SCORE = D.SCORE
GROUP BY H.HACKER_ID, H.NAME
HAVING COUNT(DISTINCT S.SUBMISSION_ID) > 1
ORDER BY COUNT(DISTINCT S.SUBMISSION_ID) DESC, H.HACKER_ID
```
