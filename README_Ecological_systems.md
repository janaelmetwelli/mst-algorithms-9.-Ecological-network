# Ecological Networks & Minimum Spanning Tree Algorithms

##  Project Overview

This project aims to run five different Minimum Spanning Tree (MST) algorithms on five ecological networks having different sizes. The code analyzes, visualizes, and compares the performance of these algorithms in ecological contexts, where nodes often represent species or habitats and edges represent interactions, distances, or dependencies.


##  MST Algorithms Implemented

We implemented the following five MST algorithms:

1. *Kruskal’s Algorithm* 
   - Sorts all edges and adds the smallest edges to the MST as long as it doesn't form a cycle.
   - Time complexity: O(ElogE)
   - Space complexity: O(V+E)
   - simpler implementation than the rest of the algorithms
2. *Prim’s Algorithm*
   - Picks a node arbitrary and starts adding the neighbors with the smallest weights. 
   - It adds the smallest edges which contain only one of its vertices in the current cut.
   - Time Complexity: O(ElogV)
   - Space Complexity: O(V+E)
   - good for dense graphs
3. *Borůvka’s Algorithm*
   - a greedy algroithm that parallelly appends the cheapest edge coming out of each tree.
   - Time Complexity: O(ElogV)
   - Space Complexity: O(V+E)
   - good for parallel processing
4. *Reverse-Delete Algorithm*
   - Sorts all edges descendingly and starts removing the heaviest edges as long as it doesn't disconnect the graph
   - Time Complexity: O(E³)
   - Space Complexity: O(V+E)
5. *Karger’s Algorithm (MST variant)*
   - A randomized algorithm that repeatedly contracts edges to shrink the graph, giving an approximate solution to the MST. It’s fast and clever, but its results can vary each time due to its randomness.
   - Time Complexity:O(I × E) in our code I=100 ~O(E)
   - Space Complexity: O(E+V)

##  Dataset Overview

We worked with 5 ecological network datasets:

## *eco-florida*:
- eco-florida dataset is a foodweb nodes where each node represents a species or a group of specices 
- the edges represent an interaction relationship between a predator and a prey
- the weights represents the magnitude of the carbon flow passed from the prey to the predator.
##  *G12*: 
- This is a graph with interconnected 800 nodes that doesn’t represent anything   real.
- Nodes here act as a sort of grid where each node has connections to its immediate neighbours above, below and to either side of it.
- weights are assigned randomly (1 & -1).
- The graph was created purely for science and doesn’t have any real world meaning
## *Dubcova1*
## *GaAsH6*
## *FullChip*

Each dataset was represented as a weighted undirected graph.

## Applications 

- Sensor Network Monitoring system: Grid-like sensor system where connections between nodes serve as a simplified model for testing or studying how such networks might behave or respond to changes in real-world scenarios.
- Biodiversity assessment: MSTs can be used for Biodiversity assessment to simplify the interaction networks and remove redundent interactions ,also it helps to find the keystone species, whose removal impacts the system greatly.
- Ecosystem Modeling: MSTs contribute in the ecosystem modeling as it highlights the fundamental structural backbone of the system and shows the main lines through which energy must pass through from producers to top predators. 
- Neural Network Models: a streamlined neural network that keeps the vital local connections for processing spatial information while cutting out unnecessary links to stay efficient.