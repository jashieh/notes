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
