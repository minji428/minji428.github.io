---
# multilingual  pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: Binary Tree Nodes
author: Ms. Park's Workshop
title: Binary Tree Nodes
category: SQL
tags: [sql, HackerRank]
date: 2023-02-17 20:00:00 +0900
---
<!-- 소제목 -->
<!-- outline-start -->
<a href="https://www.hackerrank.com/challenges/binary-search-tree-1/problem">Binary Tree Nodes</a>
<!-- outline-end -->

<h2>문제</h2>
<img src="/assets/img/posts/sql/Binary_Tree_Nodes1.jpg" title="Binary_Tree_Nodes1.jpg" alt="Binary_Tree_Nodes1.jpg"/><br>
<img src="/assets/img/posts/sql/Binary_Tree_Nodes2.jpg" title="Binary_Tree_Nodes2.jpg" alt="Binary_Tree_Nodes2.jpg"/><br>

<h2>코드</h2>
<h3>Oracle</h3>

```sql
SELECT DISTINCT BST.N
    , CASE
        WHEN BST.P IS NULL THEN 'Root'
        WHEN BST2.n IS NULL THEN 'Leaf'        
        ELSE 'Inner'
    END
FROM BST
    LEFT JOIN BST BST2 ON BST.N = BST2.P
ORDER BY BST.N
```

<h2>참고사항</h2>
root가 될려면 N컬럼엔 있으며 P컬럼 안에 값이 없어야 가능(null) <br/>
inner <br/>
leaf가 되려면 자식이 없어야 가능, P컬럼에서 없어야 함 <br/>