# Hamiltonian Path in DAG
    
        <nobr></nobr>

## Problem


A Hamiltonian path is a path in a graph that visits each vertex exactly once.
Checking whether a graph contains a Hamiltonian path is a well-known hard problem.
At the same time it is easy to perform such a check if a given graph is a DAG.
**Given:** A positive integer $k \le 20$ and $k$ simple directed acyclic graphs in the edge list format with at most $10^3$ vertices each.


**Return:** For each graph, if it contains a Hamiltonian path output "1" followed by a Hamiltonian path (i.e., a list of vertices), otherwise output "-1".
