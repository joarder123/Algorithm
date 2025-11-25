Knight Moves (BFS in 2D Grid) — Shortest Path of a Knight
🔍 Problem Description

The goal of this problem is to compute a classic shortest path on a chessboard.

Given two squares a and b, determine:

➡️ What is the minimum number of knight moves required to travel from a to b?

We can model this as a shortest path problem on an unweighted graph.

🎯 Graph Modeling
Concept	Meaning
Nodes	The 64 squares of the chessboard
Edges	A valid knight move between two squares
Cost	Each move costs 1 step

Since all edges have equal weight, the best algorithm to solve this is:

✅ Breadth-First Search (BFS)

🧠 What is BFS?

BFS (Breadth-First Search) is a graph traversal algorithm that explores nodes level by level starting from the source node.

It uses a Queue and ensures that the first time we reach a node, we reach it using the shortest possible path.

This makes BFS the ideal solution for finding the shortest path in an unweighted graph like this knight problem.
