# Dynamic Array Data Structure

## Introduction

A **dynamic array** is an array that resizes itself automatically when an element is added or removed. It provides random access and allows for efficient insertion and deletion operations.

## Characteristics of Dynamic Arrays

- **Resizable**: Automatically resizes itself when the capacity is reached.
- **Random Access**: Allows direct access to any element using the index.
- **Flexible Size**: Can grow or shrink as needed.

## Basic Operations

1. **Insert**: Adds an item to the array.
2. **Delete**: Removes an item from the array.
3. **Get**: Retrieves an item from the array using an index.
4. **Set**: Updates an item at a specific index.
5. **Size**: Returns the number of elements in the array.

## Applications of Dynamic Arrays

- Storing dynamic data where the size can change
- Implementing other data structures like stacks, queues, and lists
- Efficient memory usage in various algorithms

## Java Implementation Using Inbuilt ArrayList

Java provides an inbuilt `ArrayList` class as part of the `java.util` package, which implements the List interface. Here's a simple Java implementation using this class:

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Create an ArrayList
        ArrayList<Integer> dynamicArray = new ArrayList<>();

        // Insert elements
        dynamicArray.add(10);
        dynamicArray.add(20);
        dynamicArray.add(30);
        dynamicArray.add(40);
        dynamicArray.add(50);

        // Display the ArrayList
        System.out.println("ArrayList: " + dynamicArray);

        // Insert element at a specific index
        dynamicArray.add(2, 25);
        System.out.println("After adding element at index 2: " + dynamicArray);

        // Remove element at a specific index
        dynamicArray.remove(4);
        System.out.println("After removing element at index 4: " + dynamicArray);

        // Get element at a specific index
        int element = dynamicArray.get(3);
        System.out.println("Element at index 3: " + element);

        // Set element at a specific index
        dynamicArray.set(1, 15);
        System.out.println("After setting element at index 1: " + dynamicArray);

        // Get the size of the ArrayList
        int size = dynamicArray.size();
        System.out.println("Size of the ArrayList: " + size);

        // Traverse the ArrayList
        System.out.println("Traversing the ArrayList:");
        for (int value : dynamicArray) {
            System.out.print(value + " ");
        }
    }
}
