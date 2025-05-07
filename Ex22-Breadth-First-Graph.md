# Ex22 Breadth First Graph
## DATE:15-04-2025
## AIM:
To write a printQueue C function of the given graph that is to be traversed in the breadth first manner.

![image](https://github.com/user-attachments/assets/f483f48c-6af0-4027-a993-01c108a50933)


## Algorithm
1. Start the program.
2. Check if the queue is empty using isEmpty(q). If true, print "Queue is empty".
3. If not empty, print "Queue contains ".
4. Initialize a loop variable i to q->front.
5. Use a for loop to iterate from q->front to q->rear, printing each item in q->items[i].
6. End the loop and function after printing all items.
7. End the program.  

## Program:
```
/*
Program to traverse graph using BFS
Developed by: SAKTHIVEL S
RegisterNumber:  212223220090
*/
void printQueue(struct queue* q) {
  int i = q->front;
 
  if (isEmpty(q)) {
    printf("Queue is empty");
  } else { 
    printf("Queue contains ");
    for (i = q->front; i < q->rear + 1; i++) {
      printf("%d ", q->items[i]);
    }
   }
}
```

## Output:

![image](https://github.com/user-attachments/assets/0d04d2af-0fc0-459a-b584-f6e9b5736bd4)


## Result:
Thus, the code for the printQueue function of the following graph that is to be traversed in the breadth first manner is implemented successfully.
