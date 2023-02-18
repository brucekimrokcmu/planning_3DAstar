# planning

This work is to implement a planner where a point robot intercepts a moving target in a 2D grid map. 
The robot can move in 8-connected grid, and each cell has a cost value. 

To catch the moving target, I first implemented a look up table of backward Dijkstra to calculate g* value of all cells to the closest goal in the goal trajectory. I referred to the look up table for my heuristics in 2D weighted AStar search.

The data structure I used for open list is prioirty queue that sorts by lower F-values and unordered_map for closed list, vistied list, and heuristics map.
