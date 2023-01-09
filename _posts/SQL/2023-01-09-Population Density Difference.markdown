---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Population Density Difference

# 제목
title: Population Density Difference

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
date: 2023-01-09 20:34:00 +0900

---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/population-density-difference/problem?h_r=internal-search">Population Density Difference</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Population_Density_Difference.JPG" title="Population_Density_Difference.JPG" alt="Population_Density_Difference.JPG"/><br>

<h2>코드</h2>
<h3>MySQL</h3>

```sql
SELECT MAX(POPULATION) - MIN(POPULATION)
FROM CITY
```
