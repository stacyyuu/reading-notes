## Data Structures and Algorithms

- **Data Structures** are a specialized means of organizing and storing data in computers in such a way that we can perform operations on the stored data more efficiently. 
- Data Structures have a wide and diverse scope of usage across the fields of Computer Science and Software Engineering. 
- **8 Common Data Structures**:
- An **array** is a structure of fixed-size, which can hold items of the same data type. 
- **Array operations**: Traverse - go through the elements and print them. Search - search for element in array by value or index. Update - update value of an existing element at a given index. 
- **Linked Lists**: sequential structure that consists of a sequence of items in linear order which are linked to each other. Hence, you have to access the data sequentially and random access is not possible.
- **Linked list operations**: Search - find first element with the key **k** in the given linked list by a simple linear search. Insert - insert a key to the linked list. Beginning, middle, or end. Delete - removes an element **x** from a given linked list. 
- **Stacks** is a LIFO (Last In First Out - the element placed at last can be accessed at first) structure which can be commonly found in many programming languages.
- **Stacks operations**: Push - insert element at top of stack. Pop - delete the topmost element and return it. 
- **Queues** is a FIFO (First In First Out - the element placed at first can be accessed first) structure which can be commonly found in many programming languages. 
- **Queue operations**: Enqueue - insert an element to the end of the queue. Dequeue - delete the element from the beginning of the queue. 
- **Hash Table** is a data structure that stores values which have keys associated with each of them. 
- **Tree** is a hierarchical structure where data is organized hierarchically and are linked together. 
- **Heaps** is a special case of a binary tree where the parent nodes are compared to their children with their values and are arranged accordingly.
- **Graphs** consist of a finite set of **vertices** or nodes and a set of **edges** connecting these vertices. 
- **Big O** notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. 
- Big O notation describes the **complexity** of your code using algebraic terms. 

1. What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?
- Different data structure choices can have an impact on the performance of an algorithm. Depending on the choice, the right pick can lead to more efficiency. 
- Running an algorithm involves storing and manipulating data, this will require a certain number of operations to be done using it. 
- We need to choose the data structure that delivers the best performance trade-off over the tasks we have to accomplish. 
- No single data structure can be used as a solution to every problem. 

2. How can we ensure that we’ll avoid an infinite recursive call stack?
- Recursion is when a function calls itself until someone stops it. It can be used instead of a loop. If no one stops it, it'll recurse forever and crash your program. 
- A **base case** is a condition that stops the recursion. 
- Loops use extra state variables for tracking and counting, while recursion only uses the provided parameters. 

[Back to main page](README.md)
