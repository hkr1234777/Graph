# Prim's MST Algorithm in C++

## Overview
This C++ program implements Prim's algorithm to find the Minimum Spanning Tree (MST) of a graph. The graph is represented using adjacency lists and a weight matrix. The program reads the number of vertices and edges from the user, takes the edges with their respective weights as input, and computes the MST starting from a root vertex (vertex 1).

## Includes and Definitions

### Libraries Used:
- `<iostream>`: For input and output operations.
- `<vector>`: For dynamic arrays.
- `<queue>`: For priority queues.
- `<utility>`: For using the `pair` data structure.
- `<functional>`: For the `greater` comparator.
- `<unordered_set>`: For using unordered sets.

### Macro Definitions:
- `p`: Alias for `pair<int, int>`, used for representing edges.
- `pa`: Alias for `pair<int, p>`, used for representing edges with their costs.
- `infinite`: Represents an infinite value used for initialization.
- `nil`: Represents a null value for parent initialization.

## Global Variables
- `debug`: A flag for enabling or disabling debug messages.
- `Q`: An unordered set to keep track of vertices.
- `N`: Number of vertices.
- `E`: Number of edges.
- `pie`: A vector to store the parent of each vertex in the MST.
- `key`: A vector to store the minimum weight edge connecting a vertex to the MST.
- `V`: A vector to store all vertices.
- `minE`: A priority queue (min-heap) to store edges and their costs.
- `w`: A 2D matrix to store the weights of the edges.
- `G`: A 2D matrix to store the adjacency list of the graph.

## Initialization Function
The initialization function sets up the necessary data structures:
- Resizes the adjacency list and weight matrix according to the number of vertices.
- Initializes the `V` vector with vertex indices.
- Resizes the `pie` and `key` vectors to the number of vertices.

## Add to Queue Function
This function adds edges connected to a given vertex to the priority queue:
- Iterates through the adjacency list of the given vertex.
- Pushes each connected edge to the priority queue along with its cost.
- If debugging is enabled, prints information about the added edges.

## MST_PRIM Function
The `MST_PRIM` function implements Prim's algorithm:
- Initializes the `key` and `pie` vectors. All vertices are initially assigned a key value of `infinite` and a parent value of `nil`.
- Sets the key value of the root vertex to 0 and adds its edges to the priority queue.
- While the priority queue is not empty, extracts the edge with the minimum cost.
- Checks if the extracted edge provides a lower cost to connect a vertex to the MST.
- Updates the parent and key values accordingly and adds the new vertex's edges to the priority queue.

## Main Function
The main function controls the program's execution:
- Reads the number of vertices and edges from the user.
- Reads the edges and their weights, updating the adjacency list and weight matrix.
- Initializes the necessary data structures.
- Runs Prim's algorithm starting from the root vertex.
- Prints the MST and the total minimum cost.

For the complete code and more details, visit the [GitHub repository](https://github.com/Layman806-zz/MST-Prim).
