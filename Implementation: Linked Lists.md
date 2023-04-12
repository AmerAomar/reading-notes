## Big O: Analysis of Algorithm Efficiency 


### **something that I learned**

That the efficiency of an algorithm can be analyzed using Big O notation, which describes the runtime of an algorithm in terms of the size of the input. This is useful for understanding how an algorithm will perform on different types of input and for choosing the most efficient algorithm for a particular task.

I also learned about O(1) or "constant time" algorithms, which have a fixed runtime that does not depend on the size of the input, as well as O(n) or "linear time" algorithms, which have a runtime that grows proportionally to the size of the input. These concepts are important to understand for optimizing the performance of software and designing efficient algorithms.

***click Here [For Reading full article ](https://realpython.com/python-thinking-recursively/).***

An example of using Big O notation to analyze algorithm efficiency is calculating the runtime of a function that sorts an array of integers. The sorting function might have a runtime of O(n^2) if it uses a bubble sort algorithm, which compares each element of the array to every other element. However, if the sorting function uses a more efficient algorithm like quicksort, which has a runtime of O(n log n), it will be much faster for large arrays.

An example of an O(1) algorithm is accessing an element of an array by index. Regardless of the size of the array, it takes the same amount of time to access an element because the index is directly mapped to a memory address. In contrast, an example of an O(n) algorithm is searching an array for a specific value. The worst-case runtime of a linear search is proportional to the size of the array because every element might need to be checked before finding the target value.

---
## Linked Lists
### **something that I learned**

I learned that a linked list is a data structure that consists of a sequence of nodes, where each node contains some data and a reference to the next node in the sequence. Singly linked lists are a type of linked list in which each node has a reference to only the next node in the list.

One of the benefits of using a singly linked list is that it allows for constant-time insertion and deletion of elements from the list, as long as you have a reference to the node before the node you want to insert or delete. For example, if you have a singly linked list with nodes A, B, C, and D, and you want to delete node B, you would update the reference in node A to point to node C instead of node B, and then node B would be removed from the list.

Another thing I learned is that singly linked lists are not as efficient for searching for elements in the list, because you have to traverse the list one node at a time until you find the node you're looking for. This can take up to O(n) time, where n is the number of nodes in the list. In contrast, searching for elements in an array takes constant time O(1) if you know the index of the element you're looking for.

Overall, singly linked lists are useful for situations where you need to frequently insert or delete elements from the list, but not as useful for situations where you need to search for elements in the list.

***click Here [For Reading full article ](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html).***

---
## What’s a Linked List, Anyway? [Part 1]

### **something that I learned**
One important concept in linked lists is that each element, called a "node," contains a value or data, as well as a reference to the next node in the sequence. This reference is usually called a "pointer" and it connects the nodes together, forming a "linked" list.

Linked lists can be thought of as a chain of nodes, with each node pointing to the next node in the chain. This is different from arrays, where the elements are stored sequentially in memory and can be accessed by their indices.

Another important concept in linked lists is the "head" of the list, which is a reference to the first node in the list. To traverse the list, we start at the head and follow the pointers from each node to the next node until we reach the end of the list.

The article also discusses the differences between "singly linked lists," where each node has a reference to only the next node in the sequence, and "doubly linked lists," where each node has references to both the next and previous nodes in the sequence.

Overall, linked lists are useful data structures for situations where we need to insert or remove elements frequently, as this can be done efficiently by adjusting the pointers between the nodes. However, searching for elements in a linked list can be less efficient than in an array, as we need to traverse the list sequentially.

***click Here [For Reading full article ](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d).***

---

## What’s a Linked List, Anyway? [Part 2]

### **something that I learned**

 I learned about the different types of linked lists, including singly linked lists, doubly linked lists, and circular linked lists.

I also learned about the benefits and drawbacks of using linked lists. Linked lists are useful for dynamic data structures, where the size of the data can change during the execution of a program. They can also be used to implement certain types of data structures like stacks, queues, and hash tables. However, they have drawbacks as well, such as a lack of constant-time random access and the overhead of storing pointers in addition to data.

One specific example from the article that I found interesting was the use of a circular linked list to implement a round-robin scheduling algorithm in an operating system. In this algorithm, each process is assigned a time slice to run, and when that time slice expires, the process is placed at the end of the queue and the next process is allowed to run. By using a circular linked list, the algorithm can efficiently cycle through the processes and ensure that each process gets a fair share of the CPU time.

***click Here [For Reading full article ](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996).***

