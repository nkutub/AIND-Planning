# Planning Heuristic Search Results for Cargo Problem 

All three of the cargo planning problems were attempted to be solved using the following heuristic search methods: 

* astar_search h_ignore_preconditions - type 9
* astar_search h_pg_levelsum - type 10

### Metric summary

**Heuristic:**
Problem # | Search Type  | Length  | Time   | Expansions | Goal Tests | New Nodes
:------:  | :------:      | :------: | ------:| ------:    | ------:    | ------: 
 1 | 9 | 6 | .04 sec| 41 | 43 | 170 
 1 | 10 | 6 | .68 sec | 11 | 13 | 50
 2 | 9 | 9 | 4.69 sec| 1450 | 1452 | 13303 
 2 | 10 | 9 | 56.21 sec | 86 | 88 | 841
 3 | 9 | 12 | 17.58 sec| 5040 | 5042 | 44944 
 3 | 10 | 12 | 292.53 sec | 316 | 318 | 2912

I included the metrics from the non-heuristic analysis for comparison.

**Non-Heuristic:**
Problem # | Search Type  | Length  | Time   | Expansions | Goal Tests | New Nodes
:------:  | :------:      | :------: | ------:| ------:    | ------:    | ------: 
 1 | 1 | 6 | .33 sec| 43 | 56 | 180 
 1 | 3 | 12 | .01 sec | 12 | 13 | 48
 1 | 5 | 6 | .04 sec | 55 | 57 | 224
 2 | 1 | 9 | 13.09 sec| 3343 | 4609 | 30509 
 2 | 3 | 575 | 2.89 sec | 582 | 583 | 5211
 2 | 5 | 9 | 11.25 sec | 4852 | 4854 | 44030
 3 | 1 | 12 | 98.91 sec| 14663 | 18098 | 129631 
 3 | 3 | 596 | 3.21 sec | 627 | 628 | 5176
 3 | 5 | 12 | 50.17 sec | 18235 | 18237 | 159716



### Result Analysis

Here some interesting observations: 

*Optimally*

It is clear that the heuristic based searches preform better than the non-heuristic searches in generating optimal results. 

*Time taken*

Even though the h_pg_levelsum heuristic resulted in optimal results, it still took longer. This is likely due to time to generate graphplan. h_pg_levelsum was also faster than the non-heuristics searches. 

*Memory* 

Here the h_ignore_preconditions performed the best with the lowest overall Expansions. Again the graphplan is a great guide for the search algorithm to go down the correct paths but at the expense of more time to figure it out. 