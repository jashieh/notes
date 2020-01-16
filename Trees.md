What is in-order/pre-order/post-order traversal of a tree?
What is Depth-first/ breath-first search of a tree?


Binary Search Tree
* Left child is less than
* Right child is greater than or equal to parent

How does a tree balance itself?

Are recursive calls on the call stack considered towards space complexity?

# Heaps
What is a heap?
* A partially ordered data structure.
* Root of tree is either max or min (max or min heap)

## Max Heap
* Children of a node are less than or equal to parent

## Min Heap
* Children of node are greater than or equal to parent

What are the implications of heap data structure?
* In a max heap, the root will be greater than its children, grandchildren, etc. recursively

How do you insert into a heap?
* Insert at farther left as possible then swap up to furfil heap property.

How do you delete from a heap?
* Delete Node
* Pick farther right node in heap
* Swap with larger child for max heap, smaller child for min heap recursively

How do you represent a heap as an array?
* Node = i 
* Parent = i/2
* Left child = 2*i + 1
* Right Child = 2*i + 2
* Ex: [42, 32, 24]

## Heap Sort
* Insert into heap
* Delete the root from heap and store the value until heap is empty

## Heap Sort in place
* Store sorted part at end of array
* Store length of heap and sorted array, operate on unsorted part


What is a complete Tree? 
* All levels besides bottom level is filled with nodes
* Bottom level has children filled to the left as much as possible

# Tries (aka prefix tree)
Search tree used to efficiently store a set of strings for later retrieval.

## What makes a Trie different than a normal tree
* Tries store values in their edges instead of on the nodes.

## Why use Tries?
* Tries are more efficient than hash-tables for strings as lookup time is based on the length of the word while the worst
case for a hash would be the size of the table due to collisions.
