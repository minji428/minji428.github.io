---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: New Companies
author: Ms. Park's Workshop
title: New Companies
category: SQL
tags: [sql, HackerRank]
date: 2023-01-29 20:14:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/the-company/problem">New Companies</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/New_Companies1.jpg" title="New_Companies1.jpg" alt="New_Companies1.jpg"/><br>
<img src="/assets/img/posts/sql/New_Companies2.jpg" title="New_Companies2.jpg" alt="New_Companies2.jpg"/><br>
<img src="/assets/img/posts/sql/New_Companies3.jpg" title="New_Companies3.jpg" alt="New_Companies3.jpg"/><br>
<img src="/assets/img/posts/sql/New_Companies4.jpg" title="New_Companies4.jpg" alt="New_Companies4.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT C.COMPANY_CODE
     , C.FOUNDER
     , COUNT(DISTINCT L.LEAD_MANAGER_CODE)
     , COUNT(DISTINCT S.SENIOR_MANAGER_CODE)
     , COUNT(DISTINCT M.MANAGER_CODE)
     , COUNT(DISTINCT E.EMPLOYEE_CODE)
FROM COMPANY C
    LEFT JOIN Lead_Manager L ON C.COMPANY_CODE = L.COMPANY_CODE
    LEFT JOIN Senior_Manager S ON L.COMPANY_CODE = S.COMPANY_CODE
    LEFT JOIN Manager M ON S.COMPANY_CODE = M.COMPANY_CODE
    LEFT JOIN Employee E ON M.COMPANY_CODE = E.COMPANY_CODE
GROUP BY C.COMPANY_CODE, C.FOUNDER
ORDER BY C.COMPANY_CODE
```
```SQL
SELECT C.COMPANY_CODE
     , C.FOUNDER
     , COUNT(DISTINCT L.LEAD_MANAGER_CODE)
     , COUNT(DISTINCT S.SENIOR_MANAGER_CODE)
     , COUNT(DISTINCT M.MANAGER_CODE)
     , COUNT(DISTINCT E.EMPLOYEE_CODE)
FROM  COMPANY C
    , Lead_Manager L
    , Senior_Manager S
    , Manager M
    , Employee E
WHERE C.COMPANY_CODE = L.COMPANY_CODE
    , L.COMPANY_CODE = S.COMPANY_CODE
    , S.COMPANY_CODE = M.COMPANY_CODE
    , M.COMPANY_CODE = E.COMPANY_CODE
GROUP BY C.COMPANY_CODE, C.FOUNDER
ORDER BY C.COMPANY_CODE;
```