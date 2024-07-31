# Priority Queue Data Structure

## Introduction

A **priority queue** is a special type of queue in which each element is associated with a priority and is served according to its priority. If elements with the same priority occur, they are served according to their order in the queue.

## Basic Operations

1. **Insert (Enqueue)**: Adds an item to the priority queue. The position is determined by the priority of the element.
2. **Remove (Dequeue)**: Removes the item with the highest priority.
3. **Peek**: Returns the item with the highest priority without removing it.
4. **isEmpty**: Returns true if the priority queue is empty, false otherwise.

## Applications of Priority Queue

- Scheduling processes in operating systems
- Managing tasks in printing spools
- Pathfinding algorithms like Dijkstra's algorithm
- Implementing other data structures like heaps

## Java Implementation

### Custom Implementation

Here's a simple Java implementation of a priority queue using a max-heap:

```java
import java.util.PriorityQueue;

public class Main {
    public static void main(String[] args) {
        PriorityQueue<Integer> pq = new PriorityQueue<>((a, b) -> b - a); // Max-heap

        // Insert elements
        pq.offer(10);
        pq.offer(20);
        pq.offer(30);
        pq.offer(40);
        pq.offer(50);

        // Peek at the highest priority element
        System.out.println("Highest priority element is: " + pq.peek());

        // Remove elements
        while (!pq.isEmpty()) {
            int value = pq.poll();
            System.out.println("Removed element: " + value);
        }

        // Attempting to remove from an empty priority queue will return null
        Integer value = pq.poll();
        if (value == null) {
            System.out.println("Priority queue is empty. Cannot remove.");
        }
    }
}
