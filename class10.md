# Stacks and Queues

## What is a Stack?

A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

## what is a Queue?

A queue is a data structure that consists of Nodes. Each Node references the next Node in the queue, but does not reference its previous

Stacks and queues are two types of linear data structures commonly used in computer science. The main difference between them is in how they handle the removal of elements from the data structure.

A stack is a Last-In-First-Out (LIFO) data structure. This means that the last element added to the stack is the first one to be removed. Think of a stack of plates: when you add a new plate to the stack, you place it on top of the other plates. When you need to remove a plate, you take the one on top first. In programming, a stack is often used for tasks that involve undoing or reversing actions, such as the back button in a web browser.

A queue, on the other hand, is a First-In-First-Out (FIFO) data structure. This means that the first element added to the queue is the first one to be removed. Think of a queue of people waiting in line: the first person in line is the first one to be served. In programming, a queue is often used for tasks that involve processing tasks in the order they were received, such as a print spooler.

Both stacks and queues can be implemented using arrays or linked lists. In an array implementation, a stack or queue is simply a fixed-size array with pointers to the top or front of the data structure. In a linked list implementation, each element in the stack or queue points to the next one in the list.

An example of a task that might be better suited for a stack is the undo functionality in a text editor. When a user performs an action such as typing, the editor can push the current state of the document onto a stack. If the user wants to undo their last action, the editor can simply pop the most recent state from the stack and restore it as the current state.

An example of a task that might be better suited for a queue is a print spooler. When multiple print jobs are sent to a printer, they need to be processed in the order they were received. The printer can use a queue to store the print jobs in the order they were received and process them one by one in that order.

to read the article click [here](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html).
