---
id: sp
title: "Shortest Paths"
author: Benjamin Qi
prerequisites: 
 - 
     - Gold - Breadth First Search
---

<module-excerpt>

- Shortest Path Without Negative Edge Weights
 - Shortest Path With Negative Edge Weights
 - All Pairs Shortest Path

</module-excerpt>

## Non-Negative Edge Weights

Use *Dijkstra's Algorithm*.

### Standard

 - [Kattis SSSP Non-Negative](https://open.kattis.com/problems/shortestpath1)
 - [CSES Shortest Routes I](https://cses.fi/problemset/task/1671)

### Tutorial

 - CSES 13.2
 - [cp-algo Dijkstra (Dense Graphs)](https://cp-algorithms.com/graph/dijkstra_sparse.html)
 - [cp-algo Dijkstra (Sparse Graphs)](https://cp-algorithms.com/graph/dijkstra_sparse.html)
   - Usually, it's this one that's applicable.
 - [CPC.8](https://github.com/SuprDewd/T-414-AFLV/tree/master/08_graphs_2)

### Problems 

 - CSES
   - [CSES Flight Discount](https://cses.fi/problemset/task/1195)
   - [CSES Flight Routes](https://cses.fi/problemset/task/1196)
   - [CSES Investigation](https://cses.fi/problemset/task/1202)
 - USACO
   - [Milk Pumping](http://www.usaco.org/index.php?page=viewproblem2&cpid=969)
     - fairly standard application
   - [Shortcut](http://usaco.org/index.php?page=viewproblem2&cpid=899)
   - [Fine Dining](http://usaco.org/index.php?page=viewproblem2&cpid=861)
 - Other
   - [Lane Switching](https://open.kattis.com/contests/acpc17open/problems/laneswitching)
   - [Robot Turtles](https://open.kattis.com/problems/robotturtles) [](100)

## All Pairs Shortest Path (APSP)

Use the *Floyd-Warshall* algorithm.

### Standard

 - [CSES Shortest Routes II](https://cses.fi/problemset/task/1672)
 - [Kattis APSP (with negative weights)](https://open.kattis.com/problems/allpairspath)

### Tutorial

 - CPH 13.3
 - [cp-algo Floyd-Warshall](https://cp-algorithms.com/graph/all-pair-shortest-path-floyd-warshall.html)

### Problems

 - [USACO Moortal Cowmbat](http://usaco.org/index.php?page=viewproblem2&cpid=971)
   - Use APSP before running DP.
 - [SPOJ Arbitrage](https://www.spoj.com/problems/ARBITRAG/)

## Negative Edge Weights

 - Hasn't appeared in recent USACO Gold as far as I know. 
 - Usually Bellman-Ford is used. 
 - If no negative cycles, can use [Shortest Path Faster Algorithm](https://en.wikipedia.org/wiki/Shortest_Path_Faster_Algorithm) or modify Dijkstra slightly (though the same running time bound no longer applies).

### Tutorial
 
 - [cp-algo Bellman Ford](https://cp-algorithms.com/graph/bellman_ford.html)
 - [Topcoder Graphs Pt 3](https://www.topcoder.com/community/data-science/data-science-tutorials/introduction-to-graphs-and-their-data-structures-section-3/)

You can also use shortest path algorithms to solve the following problem (a very simple [linear program](https://en.wikipedia.org/wiki/Linear_programming)).

> Given variables $x_1,x_2,\ldots,x_N$ with constraints in the form $x_i-x_j\ge c$, compute a feasible solution.

 - [Linear Programming Trick](https://www.cs.rit.edu/~spr/COURSES/ALG/MIT/lec18.pdf)

### Problems

 - General
   - [CSES High Score](https://cses.fi/problemset/task/1673)
   - [Kattis SSSP Negative](https://open.kattis.com/problems/shortestpath3)
   - [CSES (Negative) Cycle Finding](https://cses.fi/problemset/task/1197)
 - Simple Linear Programming
   - [Restore Array](https://oj.uz/problem/view/RMI19_restore)
   - [Art](https://codeforces.com/gym/102394/problem/A) (basically same as above)
   - Timeline (Camp)
     - equivalent to [Timeline (Gold)](http://www.usaco.org/index.php?page=viewproblem2&cpid=1017) except $N,C\le 5000$ and negative values of $x$ are possible.