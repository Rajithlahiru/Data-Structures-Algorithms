
# Stack Data Structure

## Introduction

A **stack** is a linear data structure that follows a particular order in which operations are performed. The order may be **LIFO (Last In First Out)** or **FILO (First In Last Out)**. In a stack, the element added last is the first one to be removed.

## Basic Operations

1. **Push**: Adds an item to the stack. If the stack is full, it is said to be an overflow condition.
2. **Pop**: Removes an item from the stack. The items are popped in the reverse order in which they are pushed. If the stack is empty, it is said to be an underflow condition.
3. **Peek or Top**: Returns the top element of the stack without removing it.
4. **isEmpty**: Returns true if the stack is empty, false otherwise.

## Applications of Stack

- Expression evaluation and syntax parsing
- Backtracking algorithms
- Function call management in recursion
- Undo mechanisms in text editors

## Java Implementation using Inbuilt Stack

Here's a simple Java implementation of a stack using Java's inbuilt `Stack` class:

```java
import java.util.Stack;

public class Main {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        // Push elements onto the stack
        stack.push(10);
        stack.push(20);
        stack.push(30);
        stack.push(40);
        stack.push(50);

        // Attempting to push another element will not show an error, 
        // as the built-in Stack does not have a fixed size limit by default
        stack.push(60);

        // Peek at the top element
        System.out.println("Top element is: " + stack.peek());

        // Pop elements from the stack
        while (!stack.isEmpty()) {
            int value = stack.pop();
            System.out.println("Popped element: " + value);
        }

        // Attempting to pop from an empty stack will throw an EmptyStackException
        try {
            stack.pop();
        } catch (java.util.EmptyStackException e) {
            System.out.println("Stack is empty. Cannot pop.");
        }
    }
}
