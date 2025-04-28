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

Total work = O(dlog<sub>d</sub>|V| + |E|log<sub>d</sub>|V|)


- **1d.**


- **2a.**


- **2b.**


- **2c.**

- **2d.**

- **2e.**



- **3a.**


- **3b.**


- **3c.**
