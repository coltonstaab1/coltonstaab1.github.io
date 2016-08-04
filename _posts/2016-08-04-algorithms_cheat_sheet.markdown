---
layout: post
title:  "Algorithms cheat sheet"
date:   2016-08-04 18:07:29 +0000
---

I know that many coding bootcamp students often struggle with the algorithms part of coding interviews, so I decided to take the [Udacity algorithms class](https://www.udacity.com/course/technical-interview--ud513). This post is a review of the key concepts from that class. I'm planning to use this cheat sheet for myself as I prep for whiteboard coding interviews and am hoping that other students at Flatiron find this helpful as well!

## General concepts:
* **Approximations:** approximate equations are those that approximate the runtime of an algorithm. Approximation equations drop the less important terms in equations; e.g. O(n^2 + 2n + 1) becomes O(n^2)
* **Best, average, and worst case efficiency:** with algorithms, you often want to know how the algorithm will perform in difference circumstances. As a result, you often want to evaluate its performance in the best, average, and worst-case scenarios
* **Big-O notation:** big-O notation is a term that's used to refer to refer the time and space efficiency associated with an algorithm.
* **Efficiency:** efficiency refers to how much time and how many computing resources an algorithm requires to solve a particular problem
* **Greedy algorithms:** greedy algorithms are those choose whatever option looks best at any particular point in the algorithm's progression
* **Hashing collisions:** hashing collisions occur when two different inputs yield the same output
* **Hashing functions:** hashing functions is one where you apply it to an input and the function returns an output that makes it easily searchable
* **Hashing load factor:** load factor is: (# entries/# buckets) for a hashing algorithm. If the load factor is greater than 1, there will definitely be collisions, but the closer it gets to zero, the more wasteful the algorithm is
* **Knapsack problem:** this is a common interview question about maximization. You have a knapsack with a limited weight capacity and objects that have a value and weight associated with them; the goal is to maximize the value of the items you fit into the knapsack
* **Recursion:** recursive functions must meet two basic criteria: 1) that the function references itself, and 2) that there's a base case with which the function starts
* **Results table:** if you're in an interview and if you're asked to determine the efficiency of an algorithm but don't have the answer memorized, you can build out a table that shows how many iterations you'd need to do given the number of inputs. You can graph out the results and look at the relationship between the number of inputs and iterations to determine the algorithm's efficiency


## Data structures:
### Graphs:
#### Terms: 
* **Core defintion:** graph is a data structure that conveys relationships between nodes. Nodes consist of values and are connected by edges. Edge objects know which nodes they connect, whether they have a direction (e.g. can only be traversed in one direction), and whether they have a weight
* **Node:** this is the base component of a graph. It has a value and an ID associated with it
* **Edge:** these are the connections between nodes in a graph. They contain information about which nodes they connect and may contain information about the strength of the relationship as well
* **Strong connectivity:** strong connectivity is where each node in the graph can reach every other node in the graph
* **Weak connectivity:** this is where all of the nodes in the graph are connected are connected to one another, but not all nodes can reach all other nodes. This often happens as a result of unidirectional relationships between nodes
* **Connectivity:** this is the minimum number of edges that would need to be removed for the graph to become disconnected 
* **Cycle:** a cycle is when yo ustart at one node, traverse the other nodes through their edges, and return to the original node
* **Directed acyclic graph:** this is a graph that doesn't have any cycles because its edges are all directed
* **Undirected graph:** this is a graph where all of the relationships between the nodes are bidirectional
* **Shortest path problem:** this is a problem wher eyou're trying to find the shortest paths between two nodes. This problem can be done on either weighted or unweighted edges
#### Implementation:
* **Adjacency matrix:** this is an A x A matrix, where A is the number of nodes in the graph. Matrix[i][j] shows you whether node i has a relationship with node j.
* **Edge list:** This is just a list of all of the edges in the graph. Each item in the list tells you which nodes are connected and the weight of the edge (if applicable)
* **Adjacency list:** this is a list of length i, where i is the number of the nodes in the graph. List[n] shows you which nodes node n shares edges with.
#### Traversal:
* **Breadth-first search:** a breadth-first search is where you search every edge of a node before moving onto the next node. The efficiency here is O(|E|+|V|), where E is the number of edges and V is the number of vertices (or nodes). This is the efficiency that results becuase you need to visit every edge and vertex during the graph traversal
* **Depth-first search:** this is a search where you pick an edge at random and keep moving down until you've run out of nodes to see. The efficiency of this method is also O(|E|+|V|) because you also need to visit every edge and vertex during your graph traversal
* **Eulerian path:** an Eulerian path is one in which you visit every path in a graph at least once and you must end at the same node you started with. Traversing an Eulerian path has an efficiency of O(|e|), where e is the number of edges
#### Algorithms:
* **Dijkstra's algorithm:** this is a solution ot the shortest path problem for graphs with weighted, undirected edges. It's a greedy algorithm with a runtime of O(|V|^2), where V is the number of vertices

### Linked-lists:
#### Terms:
* **Core definition:** a linked list is one in which each object knows its own contents as well as what come after it.  This data sturcture is easier to insert things into than an ordinary list, which is a main reason that people use linked-lists.

### Lists:
#### Terms:
* **Core definition:** in most languages, lists are basically arrays with a few additional rules. Though lists are structures that most programmers are highly familiar with, they do have a handful of computational drawbacks, including the fact that they're inefficient to insert data into.
#### Algorithms:
* **Binary search:** binary search is where you divide lists into two separate parts, evaluate whether the value you're looking for is bigger or smaller than the midpoint value. Repeat this process until you've determined whether the value is in the list. The efficiency of this approach is O(log(n))
* **Bubble sort:** this is the process of going through an array, comparing each element to the element next to it, and repeating until the array is sorted correctly. This is more efficient that naïve search, as this algorithm takes advantage of the fact that the last n elements in the array will be in the correct place after n iterations over the array. The efficiency of this algorithm is O(n) in the best case (you only need to iterate over the array of n length one time) and is O(n^2) in the average and worst cases.
* **Merge sort:** merge sort is where you sort an array by breaking it into its smallest possible elements, then merge the elements together recursively, sorting each array every time they merge. The efficiency of this algorithms in all cases is O(n * log(n))
* **Naïve search:** naïve search is when you sort an array by comparing each element in the array to the elements
* **Quick sort:** a quick sort algorithm is one in which you take a pivot (typically the last element in a list) and compare the elements before it to the pivot. Run the function recursively until the array is sorted. Efficiency: worst case: O(n^2), avg/best: O(n * log(n))

### Map:
#### Terms:
* **Core definition:** a map is a data structure defined by its key-value pairs. Maps are also commonly known as dictionaries

### Queue:
#### Terms:
* **Core definition:** a queue is basically like a double-ended stack, in which you can dequeue and enqueue things from the head and tail of the queue

### Set:
#### Terms:
* **Core definition:** a set is a list where each item is unique (e.g. there can't be two items that have the same value in a set)

### Stacks:
#### Terms:
* **Core definition:** a stack is a data structure that's basically just a pile of objects. You can see the object at the top of the stack and pop it off easily, and you can also "push" objects to the top of the stack easily. It's harder to access objects that are below the top object, however.

### Trees:
#### Terms:
* **Core definition:** a tree is an extension of a linked-list that must meet the following criteria: 1) all nodes in the tree must be connected to the other nodes in the tree, 2) There can’t be cycles in a tree (e.g. where node A refers to node B, node B refers to node C, and node C refers to node A)—you can’t go in a circle.
* **Balanced vs. imbalanced trees:** a balanced tree is one that is condensed into as few of levels as possible, while an imbalanced tree has as many levels as there are nodes (an imbalanced tree is basically a linked list)
* **Binary tree:** a binary tree is a tree in which each node has no more than 2 children. The efficiency of searching binary tree is O(n) in the best, average, and worst cases.
* **Heap:** a heap is a type of tree in which the elements are arranged according to their value; min heaps are those in which a parent always has a value lower than that of its children, while a max heap is a tree where the parents are always larger than their children
* **Red-black trees**: red-black trees are self-balancing trees that meet the following five conditions: 1) nodes are assigned an additional red/black property, 2) all nodes must have two children (even if they must be null), and all null children are black, 3) if a node is red, both children are black, 4) the root node must be black (though this is optional), 5) evert path from a node to its descendants must have the same number of black nodes
* **Self-balancing trees:** self-balancing trees algorithmically minimize the number of levels they use
#### Algorithms:
* **Binary tree insertion:** inserting a node into a binary tree has the time efficienty of O(log(n))
