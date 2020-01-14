What is a graph?

How can a graph be represented in code?
```javascript 
class GraphNode {
    constructor(val) {
        this.val = val;
        this.neighbors = [];
    }
}
```

## Adjacency Matrix
* 2D array of nodes that connect to each other
```javascript
let matrix = [
/*          A       B       C       D       E       F   */
/*A*/    [true,  true,   true,   false,  true,   false],
/*B*/    [false, true,   false,  false,  false,  false],
/*C*/    [false, true,   true,   true,   false,  false],
/*D*/    [false, false,  false,  true,   false,  false],
/*E*/    [true,  false,  false,  false,  true,   false],
/*F*/    [false, false,  false,  false,  true,   true]
];
```

## Adjacency List
* Object with node connections
```javascript
let graph = {
    'a': ['b', 'c', 'e'],
    'b': [],
    'c': ['b', 'd'],
    'd': [],
    'e': ['a'],
    'f': ['e']
};
```

How do we ensure we don't get stuck in a cycle?
* Use set to keep track of visisted nodes

# Weighted Graphs
Why do we use weighted graphs?
* To represent real life scenarios like airplane flights with different prices

# Dijkstra's Algorithm
Given a graph with weighted edges and nodes, find the shortest path from source node to another node.
