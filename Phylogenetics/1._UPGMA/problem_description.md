# Implement UPGMA
    
        <nobr></nobr>

The pseudocode for UPGMA is shown below.



UPGMA(D, n)
  Clusters ← n single-element clusters labeled 1, ... , n 
   construct a graph T with n isolated nodes labeled by single elements 1, ... , n 
 for every node v in T 
  Age(v) ← 0
 while there is more than one cluster 
  find the two closest clusters Ci and Cj  
  merge Ci and Cj into a new cluster Cnew with |Ci| + |Cj| elements
  add a new node labeled by cluster Cnew to T
  connect node Cnew to Ci and Cj by directed edges 
  remove the rows and columns of D corresponding to Ci and Cj 
  remove Ci and Cj from Clusters 
  add a row/column to D for Cnew by computing D(Cnew, C) for each C in Clusters 
  add Cnew to Clusters 
 root ← the node in T corresponding to the remaining cluster
 for each edge (v, w) in T
  length of (v, w) ← Age(v) - Age(w)
 return T


## UPGMA Problem


*Construct the ultrametric tree resulting from UPGMA.*


**Given:** An integer *n* followed by a space-delimited *n* x *n* distance matrix.


**Return:** An adjacency list for the ultrametric tree output by **UPGMA**. Weights should be accurate to three decimal places.


**Note on formatting**: The adjacency list must have consecutive integer node labels starting from 0. The *n* leaves must be labeled 0, 1, ..., *n*-1 in order of their appearance in the distance matrix. Labels for internal nodes may be labeled in any order but must start from *n* and increase consecutively.
