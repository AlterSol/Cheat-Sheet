## Introduction

Data Structures and Algorithms (DSA) are fundamental concepts in computer science that help in solving problems efficiently. A **Data Structure** is a way to organize and store data so that it can be accessed and modified efficiently. An **Algorithm** is a step-by-step procedure or formula for solving a problem. Together, they form the backbone of computer programming and software development.

Understanding DSA is crucial for software engineers, data scientists, and anyone interested in computer science as it provides a foundation for designing efficient programs and writing optimized code. This cheat sheet will provide a quick reference for some of the most commonly used data structures and algorithms, along with sample code and explanations.

## Table of Contents

1. [Data Structures](#data-structures)
   - [Arrays](#arrays)
   - [Linked Lists](#linked-lists)
   - [Stacks](#stacks)
   - [Queues](#queues)
   - [Trees](#trees)
   - [Graphs](#graphs)
   - [Hash Tables](#hash-tables)
2. [Algorithms](#algorithms)
   - [Sorting Algorithms](#sorting-algorithms)
     - [Bubble Sort](#bubble-sort)
     - [Merge Sort](#merge-sort)
     - [Quick Sort](#quick-sort)
   - [Search Algorithms](#search-algorithms)
     - [Binary Search](#binary-search)
   - [Graph Algorithms](#graph-algorithms)
     - [Depth-First Search (DFS)](#depth-first-search-dfs)
     - [Breadth-First Search (BFS)](#breadth-first-search-bfs)

---

## Data Structures

### Arrays

An array is a collection of items stored at contiguous memory locations. It is the simplest data structure where each data element can be accessed directly by using its index.

#### Example Code (Python):

```python
# Define an array
arr = [1, 2, 3, 4, 5]

# Accessing an element
print(arr[2])  # Output: 3

# Modifying an element
arr[2] = 10
print(arr)  # Output: [1, 2, 10, 4, 5]
```

### Linked Lists

A linked list is a linear data structure where each element is a separate object, called a node, containing a data field and a reference to the next node in the sequence.

#### Example Code (Python):

```python
# Node class for a linked list
class Node:
    def __init__(self, data):
        self.data = data  # Initialize the data field
        self.next = None  # Initialize the next field as None

# Linked List class
class LinkedList:
    def __init__(self):
        self.head = None  # Initialize the head of the list as None

    # Function to add a new node at the end
    def append(self, data):
        new_node = Node(data)  # Create a new node
        if self.head is None:
            self.head = new_node  # If list is empty, make new_node the head
            return
        last = self.head
        while last.next:
            last = last.next  # Traverse to the end of the list
        last.next = new_node  # Set the next of the last node to new_node

# Create a linked list and add elements
llist = LinkedList()
llist.append(1)
llist.append(2)
llist.append(3)
```

### Stacks

A stack is a linear data structure that follows the Last In First Out (LIFO) principle. It is used for undo mechanisms in text editors, browser history, etc.

#### Example Code (Python):

```python
# Stack implementation using list
stack = []

# Push elements to stack
stack.append(1)
stack.append(2)
stack.append(3)

# Pop element from stack
print(stack.pop())  # Output: 3 (LIFO: Last In, First Out)
```

### Queues

A queue is a linear data structure that follows the First In First Out (FIFO) principle. It is used in scheduling processes, managing requests in web servers, etc.

#### Example Code (Python):

```python
from collections import deque

# Queue implementation using deque
queue = deque()

# Enqueue elements
queue.append(1)
queue.append(2)
queue.append(3)

# Dequeue element
print(queue.popleft())  # Output: 1 (FIFO: First In, First Out)
```

### Trees

A tree is a non-linear data structure consisting of nodes connected by edges. It has a hierarchical structure with a root node and subtrees of children nodes.

#### Example Code (Python):

```python
# Node class for a binary tree
class TreeNode:
    def __init__(self, key):
        self.left = None  # Left child
        self.right = None  # Right child
        self.val = key  # Node value

# Creating a simple tree
root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
```

### Graphs

A graph is a non-linear data structure consisting of nodes (vertices) connected by edges. It can be used to represent networks like social networks, paths in cities, etc.

#### Example Code (Python):

```python
# Graph implementation using an adjacency list
graph = {
    'A': ['B', 'C'],
    'B': ['A', 'D', 'E'],
    'C': ['A', 'F'],
    'D': ['B'],
    'E': ['B', 'F'],
    'F': ['C', 'E']
}

# Function to add an edge to the graph
def add_edge(graph, u, v):
    graph[u].append(v)
    graph[v].append(u)
```

### Hash Tables

A hash table is a data structure that implements an associative array, a structure that can map keys to values using a hash function.

#### Example Code (Python):

```python
# Hash table implementation using dictionary
hash_table = {}

# Insert a key-value pair
hash_table['name'] = 'Alice'

# Retrieve a value by key
print(hash_table['name'])  # Output: Alice
```

## Algorithms

### Sorting Algorithms

#### Bubble Sort

Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.

#### Example Code (Python):

```python
# Bubble Sort implementation
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]  # Swap if elements are in the wrong order

# Test Bubble Sort
arr = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(arr)
print(arr)  # Output: [11, 12, 22, 25, 34, 64, 90]
```

### Search Algorithms

#### Binary Search

Binary Search is an efficient algorithm for finding an item from a sorted list of items by repeatedly dividing the search interval in half.

#### Example Code (Python):

```python
# Binary Search implementation
def binary_search(arr, x):
    low = 0
    high = len(arr) - 1
    mid = 0

    while low <= high:
        mid = (high + low) // 2
        if arr[mid] < x:
            low = mid + 1
        elif arr[mid] > x:
            high = mid - 1
        else:
            return mid  # Element found
    return -1  # Element not found

# Test Binary Search
arr = [2, 3, 4, 10, 40]
x = 10
result = binary_search(arr, x)
print(result)  # Output: 3 (Index of element 10)
```

## Conclusion

This cheat sheet provides a brief overview of essential data structures and algorithms along with their Python implementations. Understanding these fundamentals is key to solving problems efficiently in computer science.

---
