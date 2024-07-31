# Linear Search Algorithm

## Introduction

**Linear search** is a simple search algorithm that checks each element in a list sequentially until the desired element is found or the list ends. It is also known as a sequential search.

## Characteristics of Linear Search

- **Simple to Implement**: Easy to write and understand.
- **No Precondition**: Does not require the list to be sorted.
- **O(n) Time Complexity**: Checks each element, resulting in a linear time complexity.

## Basic Operations

1. **Search**: Traverse through the list to find the target element.

## Applications of Linear Search

- Searching for an element in small or unsorted lists.
- Used in scenarios where simplicity is more critical than performance.

## Java Implementation of Linear Search

Here's a simple Java implementation of the linear search algorithm:

```java
public class Main {
    public static void main(String[] args) {
        int[] array = {10, 20, 30, 40, 50};
        int target = 30;

        int index = linearSearch(array, target);

        if (index != -1) {
            System.out.println("Element " + target + " found at index " + index);
        } else {
            System.out.println("Element " + target + " not found in the array");
        }
    }

    public static int linearSearch(int[] array, int target) {
        for (int i = 0; i < array.length; i++) {
            if (array[i] == target) {
                return i;
            }
        }
        return -1; // Element not found
    }
}
