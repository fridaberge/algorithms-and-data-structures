# Assignment 0 — Sets and Complexity Analysis

Introductory coursework for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**, exploring set operations and how the choice of data structure affects an algorithm’s running time.

## Exercise 1 — Inefficient Sets

The assignment asks for a simple implementation of the abstract data type **Set**, supporting:

| Operation | Description |
| --- | --- |
| `contains(x)` | Check whether an element is present |
| `insert(x)` | Add an element if it is not already present |
| `remove(x)` | Remove an element if present |
| `size()` | Return the number of elements |

Duplicate elements are not allowed, and removing an absent element leaves the set unchanged.

The exercise intentionally uses inefficient implementations to build an understanding of linear-time operations before introducing more efficient data structures.

### Input and Output

The program reads commands from standard input:

- The first line specifies the number of operations.
- Each following line contains a command: `contains x`, `insert x`, `remove x` or `size`.
- `contains` outputs `true` or `false`.
- `size` outputs the current number of elements.
- `insert` and `remove` produce no output.

## Exercise 2 — Binary Search on a Linked List

A written exercise analysing the worst-case running time of supplied binary-search pseudocode operating on a sorted linked list.

The analysis considers:

- The operations performed inside and outside the search loop.
- The cost of accessing an element by index in a linked list.
- How the underlying data structure affects the efficiency of binary search.

Unlike an array, a linked list does not provide constant-time indexed access. Reaching an element requires traversing links, so the usual array-based binary-search complexity cannot be assumed.

## Documentation and Scope

The accompanying assignment brief describes both exercises. The written submission contains the analysis for Exercise 2.

The brief specifies the required implementation for Exercise 1; it does not by itself confirm that runnable source code is included in this folder.

## Author and Attribution

**Author:** Frida Berge

Completed for **IN2010 — Algorithms and Data Structures**, University of Oslo.

Assignment instructions and supplied pseudocode were provided by the course.
