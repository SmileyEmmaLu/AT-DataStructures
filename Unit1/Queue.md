# Queues

Queues are a data structure where elements are enqueued and dequeued in First In First Out order (FIFO). 
The data that a Queue keeps track of are it's size and a reference to the first and/or last node. 

Each node in a queue keeps track of it's data and a reference to the node in front of it \"in line\". 

The main stack operations are Enqueue-add a new node to the end of the queue, Dequeque-remove the first node of the queue and return it's data, and usually Peek- return the data of the first node of the queue without deleting it from the queque, in addition to isEmpty and size().


## Pros-
* Only accessable through FIFO
* Not easily corrupted
* Good for servers, scheduling multitasking on CPU, + much more

## Cons-
* No random access
