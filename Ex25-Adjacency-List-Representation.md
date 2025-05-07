# Ex25 Adjacency List Representation
## DATE:16-04-2025
## AIM:
To write a C program to represent the given graph using the adjacency list.

## Algorithm
1. Initialize Variables: Declare n and i as integers.
2. Read Input: Use scanf to read N (number of vertices) and n (number of edges).
3. Input Edges: Declare edges[n] of type struct Edge; use scanf to read src and dest for each edge.
4. Construct Graph: Call createGraph(edges, n) and store the result in graph. 
5. Print and Exit: Call printGraph(graph) to display the graph, then return 0.
 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: SAKTHIVEL S
RegisterNumber: 212223220090
*/

int main(void)
{   int n,i;
    scanf("%d",&N);
    scanf("%d",&n);
    // input array containing edges of the graph (as per the above diagram)
    // (x, y) pair in the array represents an edge from x to y
    struct Edge edges[n];
    for (i = 0; i < n; i++)
    {
        // get the source and destination vertex
        scanf("%d",&edges[i].src);
        scanf("%d",&edges[i].dest);
      
    }
   
    // construct a graph from the given edges
    struct Graph *graph = createGraph(edges, n);
 
    // Function to print adjacency list representation of a graph
    printGraph(graph);
 
    return 0;
}
```

## Output:

![image](https://github.com/user-attachments/assets/079abe3e-fcfe-4fe5-bd85-0db591410ede)


## Result:
Thus, the C program to represent the given graph using the adjacency list is implemented successfully
