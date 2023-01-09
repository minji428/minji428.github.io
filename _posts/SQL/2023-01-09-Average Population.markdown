---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Revising Aggregations - Average Population

# 제목
title: Revising Aggregations - Average Population

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: Ms. Park's Workshop

#카테고리 설정, 중복 불가
category: SQL

# 태그 설정, 중복 가능
tags: [sql, HackerRank]

# 대표 이미지 파일 설정
# img: ":post_pic1.jpg"

# disable comments on this page
# comments_disable: true

# 작성 날짜
date: 2023-01-09 20:30:00 +0900

---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/average-population/problem?h_r=internal-search">Revising Aggregations - Average Population</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Average_Population.jpg" title="Average_Population.JPG" alt="Average_Population.JPG"/><br>

<h2>코드</h2>
<h3>MySQL</h3>

```sql
SELECT FLOOR(AVG(POPULATION))
FROM CITY
```
