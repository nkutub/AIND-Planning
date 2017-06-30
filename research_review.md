# Planning Non-heuristic Search Results for Cargo Problem 

All three of the cargo planning prbolems were attempeted to be solved using the following non-heuristic search methods: 

* breadth_first_search
* depth_first_graph_search
* uniform_cost_search

### Metric summary
Problem # | Search Type    | Optimal           | Length  | Time   | Expansions | Goal Tests | New Nodes
:------:  | :------        | :------:           | :------: | ------:| ------:    | ------:    | ------: 
 1 | breadth_first_search | Y | 6 | .33 sec| 43 | 56 | 180 
 1 | depth_first_graph_search | N | 12 | .01 sec | 12 | 13 | 48
 1 | uniform_cost_search | Y | 6 | .04 sec | 55 | 57 | 224
 2 | breadth_first_search | Y | 9 | 13.09 sec| 3343 | 4609 | 30509 
 2 | depth_first_graph_search | N | 575 | 2.89 sec | 582 | 583 | 5211
 2 | uniform_cost_search | Y | 9 | 11.25 sec | 4852 | 4854 | 44030
 3 | breadth_first_search | Y | 12 | 98.91 sec| 14663 | 18098 | 129631 
 3 | depth_first_graph_search | N | 596 | 3.21 sec | 627 | 628 | 5176
 3 | uniform_cost_search | Y | 12 | 50.17 sec | 18235 | 18237 | 159716

### Optimal resutl summary
Action # | Problem 1 | Problem 2 | Problem 3
 :------:  | :------  | :------ | :------  
1 | Load(C1, P1, SFO) | Load(C2, P2, JFK)     | Load(C2, P2, JFK)
2 | Load(C2, P2, JFK) | Load(C1, P1, SFO)     | Load(C1, P1, SFO)
3 | Fly(P1, SFO, JFK) | Load(C3, P3, ATL)     | Fly(P2, JFK, ORD)
4 | Fly(P2, JFK, SFO) | Fly(P2, JFK, SFO)     | Load(C4, P2, ORD)
5 | Unload(C1, P1, JFK) | Unload(C2, P2, SFO) | Fly(P1, SFO, ATL)
6 | Unload(C2, P2, SFO) | Fly(P1, SFO, JFK)   | Load(C3, P1, ATL)
7 |                     | Unload(C1, P1, JFK) | Fly(P1, ATL, JFK)
8 |                     | Fly(P3, ATL, SFO)   | Unload(C1, P1, JFK)
9 |                     | Unload(C3, P3, SFO) | Unload(C3, P1, JFK)
10 |                    |                     | Fly(P2, ORD, SFO)
11 |                    |                     | Unload(C2, P2, SFO)
12 |                    |                     | Unload(C4, P2, SFO)



### Resutl Analysis

Here some interesting observations: 
* I was able to search and find solution for all three problems running on my mac within reasonable time
* There was a significat jump in time taken with very small increases in size of problem 
* Although some searches returned is faster time, they did not always yield the optimal results
* I tried some other non-huerisic searches which did not yield a result in reasonable time
* It makes sense that BFS would be more optimal than DFS since BFS test bad path and good path early vs going deep into a bad path if it was the first one selected

