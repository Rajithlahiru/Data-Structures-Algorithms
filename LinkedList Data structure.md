# Linked List Data Structure

## Introduction

A **linked list** is a linear data structure in which elements are stored in nodes. Each node contains a data part and a reference (or link) to the next node in the sequence. Unlike arrays, linked lists do not require contiguous memory locations, allowing for dynamic memory allocation and efficient insertion and deletion operations.

## Types of Linked Lists

1. **Singly Linked List**: Each node contains a reference to the next node.
2. **Doubly Linked List**: Each node contains references to both the next and previous nodes.
3. **Circular Linked List**: The last node points back to the first node, forming a circle.

## Basic Operations

1. **Insert**: Adds an item to the list.
2. **Delete**: Removes an item from the list.
3. **Search**: Finds an item in the list.
4. **Traverse**: Accesses each item in the list sequentially.

## Applications of Linked Lists

- Dynamic memory allocation
- Implementing other data structures like stacks, queues, and graphs
- Managing free space in memory

## Java Implementation Using Inbuilt LinkedList

Java provides an inbuilt `LinkedList` class as part of the `java.util` package, which implements the List interface. Here's a simple Java implementation using this class:

```java
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        // Create a LinkedList
        LinkedList<Integer> linkedList = new LinkedList<>();

        // Insert elements
        linkedList.add(10);
        linkedList.add(20);
        linkedList.add(30);
        linkedList.add(40);
        linkedList.add(50);

        // Display the LinkedList
        System.out.println("LinkedList: " + linkedList);

        // Insert element at the front
        linkedList.addFirst(5);
        System.out.println("After adding element at the front: " + linkedList);

        // Insert element at the end
        linkedList.addLast(60);
        System.out.println("After adding element at the end: " + linkedList);

        // Remove first element
        linkedList.removeFirst();
        System.out.println("After removing the first element: " + linkedList);

        // Remove last element
        linkedList.removeLast();
        System.out.println("After removing the last element: " + linkedList);

        // Get first element
        int firstElement = linkedList.getFirst();
        System.out.println("First element: " + firstElement);

        // Get last element
        int lastElement = linkedList.getLast();
        System.out.println("Last element: " + lastElement);

        // Search for an element
        boolean contains20 = linkedList.contains(20);
        System.out.println("LinkedList contains 20: " + contains20);

        // Traverse the LinkedList
        System.out.println("Traversing the LinkedList:");
        for (int element : linkedList) {
            System.out.print(element + " ");
        }
    }
}
```
