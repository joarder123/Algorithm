Second Shortest Path (Modified Dijkstra Algorithm)

Robin lives in a village that has N intersections and R bidirectional roads.
He wants to travel from intersection 1 → N, but instead of taking the shortest path, he prefers the second-shortest path.

🧠 Problem Definition

A second-shortest path means:

Its total distance is greater than the shortest path

But smaller than all other longer paths

The algorithm may reuse edges or revisit nodes

All edge weights are positive

For each test case, print:
Case X: second_shortest_path_cost

🔍 Algorithm Overview — Modified Dijkstra

For every node, we maintain two distances:

dist1[v] → shortest distance to node v

dist2[v] → second-shortest distance to node v

Relaxation rules:

1️⃣ If the new path is shorter than the current shortest:

Update dist2[v] = dist1[v]

Update dist1[v] = new distance

2️⃣ Else if
dist1[v] < new_distance < dist2[v]

Update dist2[v]

Since Dijkstra’s priority queue always expands smaller distances first,
both shortest and second-shortest distances stay correctly updated.
