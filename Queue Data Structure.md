# Queue Data Structure

## Introduction

A **queue** is a linear data structure that follows a particular order in which operations are performed. The order is **FIFO (First In First Out)**. In a queue, the element added first is the first one to be removed.

## Basic Operations

1. **Enqueue**: Adds an item to the queue. If the queue is full, it is said to be an overflow condition.
2. **Dequeue**: Removes an item from the queue. The items are removed in the same order they are added. If the queue is empty, it is said to be an underflow condition.
3. **Front**: Returns the front item from the queue without removing it.
4. **isEmpty**: Returns true if the queue is empty, false otherwise.

## Applications of Queue

- Scheduling processes in operating systems
- Handling requests in web servers
- Breadth-First Search in graphs
- Managing tasks in printing spools

## Java Implementation

### Custom Implementation

Here's a simple Java implementation of a queue using an array:

```java
import java.util.LinkedList;
import java.util.Queue;

public class Main {
    public static void main(String[] args) {
        Queue<Integer> queue = new LinkedList<>();

        // Enqueue elements
        queue.add(10);
        queue.add(20);
        queue.add(30);
        queue.add(40);
        queue.add(50);

        // Peek at the front element
        System.out.println("Front element is: " + queue.peek());

        // Dequeue elements
        while (!queue.isEmpty()) {
            int value = queue.poll();
            System.out.println("Dequeued element: " + value);
        }

        // Attempting to dequeue from an empty queue will return null
        Integer value = queue.poll();
        if (value == null) {
            System.out.println("Queue is empty. Cannot dequeue.");
        }
    }
}

