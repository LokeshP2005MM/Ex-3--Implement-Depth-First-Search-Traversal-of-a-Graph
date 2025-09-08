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
Construct a Graph with Nodes and Edges
Depth First Search Uses Stack and Recursion
Insert a START node to the STACK
Find its Successors Or neighbors and Check whether the node is visited or not
If Not Visited, add it to the STACK. Else Call The Function Again Until No more nodes needs to be visited.

# Program:
def dfs(graph, start, visited=None):
    if visited is None:
        visited = []
    visited.append(start)
    for neighbor in graph[start]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)
    return visited

# Read edges
edges = []
print("Enter edges (type 'done' to finish):")
while True:
    line = input()
    if line.lower() == "done":
        break
    u, v = line.split()
    edges.append((u, v))

# Build graph (undirected)
graph = {}
for u, v in edges:
    graph.setdefault(u, []).append(v)
    graph.setdefault(v, []).append(u)

# Print graph
print("Graph:", graph)

# Run DFS from first node in edges
start_node = edges[0][0]
print("DFS Traversal Path:", dfs(graph, start_node))


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
A B

B C

C D



### Output:
Graph: {'A': ['B'], 'B': ['A', 'C'], 'C': ['B', 'D'], 'D': ['C']}

DFS Traversal Path: ['A', 'B', 'C', 'D']



**Result:
 The above program is executed successfully.
