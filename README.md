# Ex-3-Implement-Depth-First-Search-Traversal-of-a-Graph

Name:LOKESH P

Register Number:2305001015

### Aim:
To Implement Depth First Search Traversal of a Graph using Python 3.

### Theory:

Depth First Traversal (or DFS) for a graph is like Depth First Traversal of a tree. 
The only catch here is that, unlike trees, graphs may contain cycles (a node may be visited twice). 
Use a Boolean visited array to avoid processing a node more than once. 
A graph can have more than one DFS traversal. Depth-first search is an algorithm for traversing or searching trees or graph data structures. 
The algorithm starts at the root node (selecting some arbitrary node as the root node in the case of a graph) and explores as far as possible along each branch before backtracking. 

### Algorithm:
Step 1:Construct the graph using nodes and edges (adjacency list).

Step 2:Choose a START node and push it to the stack/recursion.

Step 3:Mark the node as visited and record it in the path.

Step 4:Check its neighbors → if not visited, go deeper (push/recursive call).

Step 5:Backtrack when no neighbors left, repeat until all nodes are visited.

### Sample Input:
A B
A C
B D
B E
C E
D E

### Sample Output:

Graph: {'A': ['B', 'C'], 'B': ['A', 'D', 'E'], 'C': ['A', 'E'], 'D': ['B', 'E'], 'E': ['B', 'C', 'D']}

DFS Traversal Path: ['A', 'B', 'D', 'E', 'C']

### Input:
<img width="459" height="120" alt="Screenshot 2025-09-09 104927" src="https://github.com/user-attachments/assets/a90bef1b-400f-4730-8e17-f6e4a49c096e" />


### Output:
<img width="839" height="69" alt="Screenshot 2025-09-09 105002" src="https://github.com/user-attachments/assets/fdd1fead-db5c-4c80-983a-db5ebfdc7d59" />


### Result:
The above program is executed successfully.
