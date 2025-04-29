# CMPS 2200 Assignment 5
## Answers

**Name:** Miles Whiteford






- **1a.**
log<sub>d</sub>n

- **1b.**
delete-min: O(dlog<sub>d</sub>n)
insert: O(log<sub>d</sub>n)

- **1c.**
|V| is number of vertices, so |V| = n

delete-min = O(dlog<sub>d</sub>|V|). In Dijkstra's Algorithm, delete-min will be done at each vertex, meaning |V| times. 
Therefore work = O(|V|dlog<sub>d</sub>|V|)

insert = O(log<sub>d</sub>n). This will be done at each edge, therefore work = O(|E|log<sub>d</sub>|V|)

Total work = O(|V|dlog<sub>d</sub>|V| + |E|log<sub>d</sub>|V|)


- **1d.**
To get a value of d that yeilds a runtime of O(|E|), we must be a d in which d = |E|/|V|, meaning that the two are balanced. With the given information, this can be rewritten as $d = |V|^{1+\epsilon} / |V|$, which can be simplied to $d = |V|^{\epsilon}$. This is our answer.

- **2a.**
APSP(0,0,0) = 0
APSP(0,0,1) = 0
APSP(0,0,2) = 0
APSP(0,1,0) = n/a
APSP(0,1,1) = -2
APSP(0,1,2) = -2
APSP(0,2,0) = n/a
APSP(0,2,1) = 2
APSP(0,2,2) = -1

APSP(1,0,0) = n/a
APSP(1,0,1) = -2
APSP(1,0,2) = -2
APSP(1,1,0) = 0
APSP(1,1,1) = 0
APSP(1,1,2) = 0
APSP(1,2,0) = n/a
APSP(1,2,1) = 1
APSP(1,2,2) = 0

APSP(2,0,0) = n/a
APSP(2,0,1) = 2
APSP(2,0,2) = -1
APSP(2,1,0) = n/a
APSP(2,1,1) = 1
APSP(2,1,2) = 0
APSP(2,2,0) = 0
APSP(2,2,1) = 0
APSP(2,2,2) = 0

- **2b.**
Yes, there is a relationship. The shortest path from i to j using all vertices is either the shortest path without using vertex 2, or the path that goes through vertex 2 as an intermediate point.

- **2c.**
  
APSP(i,j,k)= min(APSP(i,j,k-1), APSP(i,k,k-1)+ APSP(k,j,k-1))

- **2d.**
  
Since there are |V|^3 possible inputs for APSP(i,j,k), checking each subproblem from scratch once O(|V|^3)

- **2e.**
Johnson's: O(|V| * |E|log<sub>d</sub>|E|)
Our dynamic programming algorithm is preferable when |E|log<sub>d</sub>|E| >> |V|^2


- **3a.**
Yes it does. This is because if an MST was not also a solution to MMET, this would mean that their exists another MST with a smaller maximum edge weight.
This condradicts the defintion of an MST, therefore a solution for MST must also be an MMET solution.

- **3b.**
Take an MST, test the removal of every edge in the MST, computing a new MST each time on the alternative tree. Then pick the tree with the smallest weight.

- **3c.**
Work of MST = O*(|E|log|E|). The worst case for my algorithm is testing every possible edge. Therefore the work is O(|E|*|E|log|E|) = O(|E|^2log|E|
