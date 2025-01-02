# Travelling Salesman Problem (TSP)

- Applied branch and bound algorithm to solve TSP problem for complete weighted graph, used MST to get the lower bound for remaining cost, and explored various heuristic approaches to achieve a nearly-optimal solution for EECS 281.
- To find the optimal tour, we started with our nearly optimal solution and then employed the brute-force method of exhaustive enumeration to achieve the optimal path while being time efficient. 

#### Note:
The images below were generated using my output files on a graph visualizer.

<p> 
  <img src="assets/Screenshot 2024-11-06 at 10.37.14 AM.png" width="100%">
  <img src="assets/Screenshot 2024-11-06 at 10.37.44 AM.png" width="100%"> 
</p>  


## Part A: Minimum Spanning Tree (MST)

Goal: Find the subset of edges that connects all vertices in a graph with the minimum total weight.

- Implemented Kruskal's and Prim's algorithms for MST construction.
- Focused on handling area-specific constraints: vertices in the Lab, Decontamination Area, and Outer Area required specific traversal rules.
- Optimized memory usage to handle graphs with tens of thousands of vertices by calculating distances on-demand instead of precomputing a distance matrix.

Output: Total MST weight and the edges used, formatted as node pairs.

## Part B: FASTTSP (Approximate TSP)

Goal: Approximate a solution to the Travelling Salesperson Problem for large graphs.

- Designed and implemented heuristics, including Nearest Neighbor and Minimum Spanning Tree-based approximations.
- Balanced runtime efficiency with solution optimality to meet autograder constraints.
- Incorporated greedy algorithms and iterative improvements to refine solutions.

Output: The approximate total tour length and the sequence of visited nodes.

## Part C: OPTTSP (Optimal TSP)

Goal: Compute the exact optimal solution for the TSP using a branch-and-bound algorithm.

- Used bounding functions to prune unpromising branches early, reducing computational overhead.
- Leveraged precomputed distance matrices for efficient edge weight lookups.
- Applied recursive permutations with intelligent pruning to guarantee the shortest tour within the time limit.

Output: The optimal tour length and the exact sequence of visited nodes.

### Note: 
Due to university policy, the code is not publicly available but can be viewed upon request.
