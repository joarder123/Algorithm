Bicoloring (BFS) — Problem Analysis
🎯 Problem: Graph Bicoloring

Given an undirected graph, determine whether it can be colored using only two colors (e.g., black and white) such that no two adjacent nodes share the same color.

🔑 Key Concept — Bipartite Graph

A graph that can be colored using two colors without conflict is called a Bipartite Graph.
In such graphs, vertices can be divided into two disjoint sets (Set A & Set B), where every edge connects a node from Set A to a node in Set B.

🚫 When Is Bicoloring Not Possible?

A graph cannot be bicolored if it contains an:

✅ Odd-Length Cycle

Example:
A triangle (cycle of length 3) cannot be bicolored.
If you assign alternate colors, the third node eventually conflicts with the first because both are adjacent.

So, odd cycles ⇒ NOT bipartite ⇒ NOT bicolorable.

🔍 Solution Strategy — Breadth-First Search (BFS)

We check bicoloring possibility using BFS traversal while assigning alternate colors to neighboring nodes.

✅ Algorithm Steps

Initialize all nodes as uncolored (-1).

Start BFS from node 0 and assign color 0.

For each visited node u, assign its neighbors the opposite color (1 - color[u]).

If any neighbor already has the same color, a conflict occurs → graph is NOT bicolorable.

If BFS finishes without conflicts → graph is BICOLORABLE.
