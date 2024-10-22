# Queue implementation

## Aim:
To use exception handling

## Theory:

Definition
A queue is a linear data structure that follows the First In, First Out (FIFO) principle. This means that the first element added to the queue will be the first one to be removed. Queues are widely used in various applications, such as scheduling processes, managing requests in a service, and handling asynchronous data.

Key Characteristics
FIFO Structure: The first element added to the queue is the first to be removed.

Operations
Enqueue: Add an element to the rear of the queue.
Dequeue: Remove and return the front element of the queue.
Peek/Front: Return the front element without removing it.
isEmpty: Check if the queue is empty.
isFull: Check if the queue is full (only applicable in fixed-size queues).

## Algorithm:

Data Structure

Define a class Queue with:

An array arr of size MAX to store queue elements.

Two integers, front and rear, initialized to -1 to track the front and rear indices.

Operations

Insert(value)

If the queue is full (check with isFull()), print "Queue overflow! Cannot insert."

If the queue is empty (check with isEmpty()), set front and rear to 0.

Otherwise, increment rear using circular indexing: rear = (rear + 1) % MAX.

Store value at arr[rear].

Print "value inserted into queue."

DeleteElement()

If the queue is empty (check with isEmpty()), print "Queue underflow! Cannot delete."

Print the element at arr[front].

If front equals rear, set both front and rear to -1 (queue becomes empty).

Otherwise, increment front using circular indexing: front = (front + 1) % MAX.

Display()

If the queue is empty (check with isEmpty()), print "Queue is empty."

Otherwise, iterate from front to rear, printing elements in the queue.

Use circular indexing to handle wrap-around.

Main Function

Create an instance of Queue.


Repeat the following until the user chooses to exit:

Display a menu with options: Insert, Delete, Display, Exit.

Read user choice.

Perform the corresponding operation based on user choice.
