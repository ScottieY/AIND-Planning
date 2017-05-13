# Analysis

## Optimal plan

### Problem 1

Load(C2, P2, JFK)
Load(C1, P1, SFO)
Fly(P2, JFK, SFO)
Unload(C2, P2, SFO)
Fly(P1, SFO, JFK)
Unload(C1, P1, JFK)

### Problem 2

Load(C2, P2, JFK)
Load(C1, P1, SFO)
Load(C3, P3, ATL)
Fly(P2, JFK, SFO)
Unload(C2, P2, SFO)
Fly(P1, SFO, JFK)
Unload(C1, P1, JFK)
Fly(P3, ATL, SFO)
Unload(C3, P3, SFO)

### Problem 3

Load(C2, P2, JFK)
Load(C1, P1, SFO)
Fly(P2, JFK, ORD)
Load(C4, P2, ORD)
Fly(P1, SFO, ATL)
Load(C3, P1, ATL)
Fly(P1, ATL, JFK)
Unload(C1, P1, JFK)
Unload(C3, P1, JFK)
Fly(P2, ORD, SFO)
Unload(C2, P2, SFO)
Unload(C4, P2, SFO)

## Comparison between non-heuristic search

### Problem 1

| Method | Expansion | Goal Tests | New Nodes | Plan Length | Time  |
| ------ | --------- | ---------- | --------- | ----------- | ----- |
| BFS    | 43        | 56         | 180       | 6           | 0.026 |
| BFTS   | 1458      | 1459       | 5960      | 6           | 0.806 |
| DFS    | 12        | 13         | 48        | 12          | 0.007 |
| DLS    | 101       | 271        | 414       | 50          | 0.075 |
| UCS    | 55        | 57         | 224       | 6           | 0.032 |
| A*IP   | 41        | 43         | 170       | 6           | 0.027 |
| A*LS   | 11        | 13         | 50        | 6           | 0.684 |

### Problem 2

| Method | Expansion | Goal Tests | New Nodes | Plan Length | Time   |
| ------ | --------- | ---------- | --------- | ----------- | ------ |
| BFS    | 3343      | 4609       | 30509     | 9           | 12.037 |
| DFS    | 1669      | 1670       | 14863     | 1444        | 11.311 |
| UCS    | 4853      | 4855       | 44041     | 9           | 10.522 |
| A*IP   | 1450      | 1452       | 13303     | 9           | 3.40   |
| A*LS   | 86        | 88         | 841       | 9           | 58.691 |

### Problem 3

| Method | Expansion | Goal Tests | New Nodes | Plan Length | Time   |
| ------ | --------- | ---------- | --------- | ----------- | ------ |
| BFS    | 14663     | 18098      | 129631    | 12          | 86.122 |
| DFS    | 592       | 593        | 4927      | 571         | 2.564  |
| UCS    | 18223     | 18225      | 159618    | 12          | 46.399 |
| A*IP   | 5040      | 5042       | 44944     | 12          | 13.86  |
| A*LS   | 325       | 327        | 3002      | 12          | 302.06 |



### Summary

For the heuristic approach, ignore_preconditions have better run-time, whereas level-sum requires less expansion, goal tests and creates less new nodes which uses less memory. Both produces optimal plans.



For the non-heuristic approach, DFS does not guarantee the optimal path, but it has the least run-time for complex problem (Problem 3), since there exist many plan that can achieve the goal. Both BFS and UCS produces the optimal plans. And UCS has the advantage in run-time in complex problems. This result was justified in Lesson 7 Search Video 23-25.