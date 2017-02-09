## Data Structures & Algorithms

## Data Structures

### Types
- Linear: order is maintained. Ex: Array, LinkedList, Stack, Queue.
- Non-Linear: Ex: Trees, Graph

## Arrays

Collection of elements. Also called with names Vectors, Tuples.
    - One dimensional array
    - Two dimensional array
    
#### Introduction
- Homogenous (all elements are of same type)
- Ordered

####Usage
- Used to implement lookup tables.
- Implement lists and Strings.
- Many databases consist of 1-D arrays whose elements are records.
- Implment heaps, hash tables, deques, queues, stacks and VLists.
- 2D Arrays are used in graph theory, Image processing and algebraic equations.

####Types of Arrays
- Static Arrays (fixed size)
  - Have O(1) insertion, deletion and reading.
  - Easy to implement.
  
- Dynamic Arrays (grow in size as array grows)
  - Flexible in size
  - Perforamance as cost for flexibility
  - Complext to implement than fixed array.
  
#### Limitations of Arrays
  - Size can't be increased or decreased during runtime.
  - Insertion and deletion on arrays are inefficient.
  - Large datasets, prog run out of memory space.
  
#### Problems on Arrays

- Find missing number in array of continuous elements from 1 to n.
- Sort a given array
- Sort elements by frequency in an array
- Merge 2 sorted arrays
- Merge 2 unsorted arrays
- Find median of 2 sorted arrays
- Max sum such that no 2 elements are adjacent
- Check if array contains a number
- Find largest and smallest number in an unsorted array
- Find pairs whose sum is equal to given sum
- Find repetitive numbers in array if it contains duplicates
- Remove duplicate elements from an array
- Find an element which repeated only once while all others repeated twice
- Find top 2 elements from unsorted array
- Rearrange positive and negetive numbers in sorted order
- Find sub array with max sum in an array of pos and neg number
- Find length of longest sequence in an array
- Reverse an array
- Find common elements in 3 sorted arrays
- Sort a 2D array by values
- Find an element in sorted 3D array

## Linked Lists 

#### Features:
 - Collection of nodes where each node contains field and address of next node.
 - First node is head node and last node is tail node.
 - Nodes are scattered in different memory blocks, need not be contiguous.
 - Compiler dynamically allocates memory space to each node.
 
#### Advantages
- Size can be dynamically increased at run time.
- Insertion and deletion are comparatively fast.

#### Disadvantages
- Pointer to next node occupy additional storage space.
- Can't be accessed directly.

#### Usages
- Trees
- Graphs
- Heaps
- Dynamic Stack
- Dynamic Queue
- Polynomials

#### Types
- Singly LL
- Doubly LL
- Circular LL
- Multi List (List containing multiple LL)

## Stack

#### Features
- Homogenous data items which are ordered.
- LIFO

#### Implementations
- Array based
- Linked List based

|Operation| Array impl | Linked List impl |
|---------|---|---|
| Create | O(1) | O(1) |
| Destroy | O(1) | O(1) |
| Push | O(1) | O(1) |
| Pop | O(1) | O(1) |
| Is empty | O(1) | O(1) | 
| Is full | O(1) | -- |

#### Usages
- Parantesis matching
- Infix to Postfix
- Stack frames for function calls
- Recursive procedures
- MS word undo redo

## Queue

#### Features
- FIFO
- Homogenous elements

#### Usages
- Printer Scheduler
- OS use queues to implement scheduling policy

#### Implementations
- Array
- Linked List

#### Priority Queue Impl
- Array 
- Linked List
- Heap based

## Tree

<img width="546" alt="tree_pic" src="https://cloud.githubusercontent.com/assets/8268939/22764760/bb1587be-ee3a-11e6-9f67-2c4a9c147e26.png">

- The depth of a node is the number of edges from the root to the node.
- The height of a node is the number of edges from the node to the deepest leaf.

#### Application of trees
- Hierarchial Structures

#### Types of binary Trees
- Ordered Search Trees: data values in left sub tree are less than right tree, no duplicates.
- Expression Tree: Represent Arthematic expression. Operands & Operators in nodes.
- Heap: Data value in any node greater than left sub tree & right sub tree. Can be used in Priority queue.

#### Binary Tree Implementation
- Array
- Linked List

#### Tree Traversal
- Breadth First Traversal:
- Depth First Traversal:
  - Pre Order: Root first, Traverse left sub tree in pre-order, then right sub tree in Pre-Order.
  - In Order: Traverse left sub tree in Inorder, then root, then right sub tree in In Order.
  - Post Order: Traverse left sub tree Post order, then Right sub tree post order, then root.
![tree_traversal](https://cloud.githubusercontent.com/assets/8268939/22766646/b99f1ee0-ee44-11e6-894a-62c2ebb146a4.jpg)

## Analysis of Algorithms
- Time complexity
- Space complexity

## Types of analysis

- Big O (worst case)
- Omega (best case)
- theta (average case)

## Asymptotic Notation

### Big O
#### Table of Important Big O

| Big O         | Common Name   | Example    |
| ------------- |:-------------:| :-----|
| O(1)      | Constant | Adding an element to start of Linked List |
| O(log n)      | logarithmic      |  Binary Search |
| O(log2n) | log squared      |    |
| O( √n ) | root n | |
| O(n) | linear | Linear search|
| O(n logn) | log linear |
| O(n²) | quadratic |  |
| O(n³) | cubic | |
| O(n4) | quadratic | |
| O(e power n) | exponential | |

// TODO: update above table

#### Example

```python
a=15                    // constant 1
b=16                    // constant 1
c=110                   // constant 1
for i in range(n):
   for j in range(n):
      x = i * i         // n²
      y = j * j         // n²
      z = i * j         // n²
for k in range(n):
   w = a*k + 450        // n
   v = b*b              // n
d = 333                 // constant 1
```
> Big O => f(n) = (1+1+1) + (n²+n²+n²) + (n+n) + 1 = (3+3n²+2n+1) = (3n²+2n+4) ≈ O(n²)

Groups of Algorithms:
- Sorting Algorithms
- Searching Algorithms
- Encoding Algorithms
- Compression Algorithms
- Iterative 
- Recursive
- Greedy
- Parsing

## Recursion

#### Usages
- Towers of hanooi
- Inorder/Preorder/Post order Tree Traversals
- DFS of Graph

#### Types
- *Tail Recursion:* If the recursive call is the last thing executed by the function.
- *Non tail recursion:* If the last thing in the function is not recursion of itself.

*Tail Recursion Example*:
```java
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```
*Not Tail Recursive:*
```java
int g(int x) {
  if (x == 1) {
    return 1;
  }

  int y = g(x-1);

  return x*y;
}
```

## Sorting Algorithms

## Bubble Sort
- 1st and 2nd elements are compared and exchanged if required.
- Do the same process till the end of the array is reached.
- For each pass, an element will be in its correct location. ie towards end of the array.

## Selection Sort
- The list contains sorted & un-sorted portions.
- Find the smallest element in the list and exchange with starting element of sorted portion.
- For each pass, the smallest element will be towards the start of the array.

## Insertion Sort
- The list contains sorted & un-sorted portions
- From 2nd element, compare with all previous elements & swap it until it reaches correct position in sorted portion.


