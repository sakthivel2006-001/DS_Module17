# Ex24 Topological Sort
## DATE:16-04-2025
## AIM:
To compose the code to determine whether the topological ordering for the following graph is possible or not.

![image](https://github.com/user-attachments/assets/c74a7111-9b59-475c-aad4-9baf23d50ec0)


## Algorithm
1. Initialize and Create Graph: Declare variables i, v, count, topo_order[MAX], indeg[MAX] and call create_graph().
2. Calculate Indegree: For each vertex i from 0 to n-1, compute indeg[i] using indegree(i) and insert into queue if indeg[i] == 0.
3. Topological Sorting: Set count = 0; while the queue is not empty and count < n, remove vertex v, add to topo_order, and update neighbors' indegree.
4. Cycle Detection: If count < n, print a cycle warning and exit. 
5. Output Order: Print "Vertices in topological order are:" followed by topo_order[1] to topo_order[count], then return 0.


## Program:
```
/*
Program to determine whether the topological ordering for the following graph is possible or not
Developed by:SAKTHIVEL S
RegisterNumber: 212223220090
*/

int main()
{
        int i,v,count,topo_order[MAX],indeg[MAX];

        create_graph();

        /*Find the indegree of each vertex*/
        for(i=0;i<n;i++)
        {
                indeg[i] = indegree(i);
                if( indeg[i] == 0 )
                        insert_queue(i);
        }

        count = 0;

        while(  !isEmpty_queue( ) && count < n )
        {
                v = delete_queue();
        topo_order[++count] = v; /*Add vertex v to topo_order array*/
                /*Delete all edges going from vertex v */
                for(i=0; i<n; i++)
                {
                        if(adj[v][i] == 1)
                        {
                                adj[v][i] = 0;
                                indeg[i] = indeg[i]-1;
                                if(indeg[i] == 0)
                                        insert_queue(i);
                        }
                }
        }

        if( count < n )
        {
                printf("No topological ordering possible, graph contains cycle\n");
                exit(1);
        }
        printf("Vertices in topological order are :\n");
        for(i=1; i<=count; i++)
                printf( "%d ",topo_order[i] );
        printf("\n");

        return 0;
}

```

## Output:


![image](https://github.com/user-attachments/assets/42eee6e6-1911-4dba-b57d-a0f86b740df8)

## Result:
Thus, the C program for determining whether the topological ordering for the following graph is possible or not, is implemented successfully.
