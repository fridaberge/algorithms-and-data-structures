# Algorithms and Data Structures

Coursework exploring trees, queues, sorting and hashing for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**.

The repository contains source code, assignment briefs, datasets, test files and written submissions.

> **Missing assignment:** This repository contains assignments 0–2 and 4. Assignment 3 covered graphs and pathfinding, but its files are no longer available and are therefore not included.

## Assignments

| Assignment | Topics | Documentation |
| --- | --- | --- |
| [Assignment 0](./Oblig0/) | See assignment files | — |
| [Assignment 1](./Oblig1/) | Binary search trees, teque, tree paths and balanced insertion orders | [README](./Oblig1/README.md) |
| [Assignment 2](./Oblig2/) | Sorting algorithms, operation counting and performance experiments | [README](./Oblig2/README.md) |
| [Assignment 4](./Oblig4/) | Hash-based sets, membership checks, insertion and removal | [README](./Oblig4/README.md) |

## Repository Structure

```text
algorithms-and-data-structures/
├── README.md
├── Oblig0/
├── Oblig1/
│   ├── Oppgave1/
│   ├── Oppgave2/
│   ├── Oppgave3/
│   ├── Oppgave4/
│   ├── IN2010-innleveringsoppgave1.txt
│   └── oppgavebeskrivelse.pdf
├── Oblig2/
│   ├── Oblig2/
│   │   ├── Java source files
│   │   ├── Input datasets
│   │   └── IN2010-innlevering2.pdf
│   └── oppgavebeskrivelse.pdf
└── Oblig4/
    ├── Oblig4/
    │   ├── Java source files
    │   ├── input/
    │   └── output/
    └── Assignment briefs
```

The READMEs for assignments 1, 2 and 4 provide file descriptions and further instructions.

## Assignment 0

[View Assignment 0 →](./Oblig0/)

## Assignment 1 — Data Structures and Trees

Four exercises introducing:

- Set operations using a binary search tree.
- A triple-ended queue with front, middle and back insertion.
- Finding the path from a tree node to its root.
- Generating insertion orders that produce balanced search trees.

Pseudocode, explanations and complexity analysis are available in the [written submission](./Oblig1/IN2010-innleveringsoppgave1.txt).

[View Assignment 1 →](./Oblig1/)

## Assignment 2 — Sorting and Performance

Java implementations of:

- Insertion sort.
- Selection sort.
- Quicksort.
- Merge sort.

The assignment checks sorted output and measures comparisons, swaps and execution time across random and nearly sorted inputs.

The [submitted report](./Oblig2/Oblig2/IN2010-innlevering2.pdf) documents the counting conventions, experiments and charts.

[View Assignment 2 →](./Oblig2/)

## Assignment 4 — Sets with Hashing

An optional exercise implementing a hash-based set with:

- `contains`
- `insert`
- `remove`
- `size`

The folder includes Java source files and input/output pairs for checking the program's results.

[View Assignment 4 →](./Oblig4/)

## Building and Running

The Java exercises require a **Java Development Kit (JDK)**.

Compile and run programs from their individual source folders. There is no repository-wide build system or shared entry point.

For example, from the repository root:

```bash
cd Oblig4/Oblig4
javac AapenHashing.java HashList.java
java AapenHashing < input/example
```

To compare the result with the expected output:

```bash
java AapenHashing < input/example > actual_example.txt
diff output/example actual_example.txt
```

See the individual assignment READMEs for input formats, source locations and available execution instructions.

## Documentation and Scope

This repository preserves coursework and supporting material rather than providing a single application or reusable algorithms library.

Assignment briefs describe the required tasks; they do not by themselves establish that every task is implemented. Written reports and archived results document the original submissions, not independently verified correctness or performance.

Compiled `.class` files can be regenerated from the Java sources.

## Author and Attribution

**Author:** Frida Berge (`fridatbe`)

Completed for **IN2010 — Algorithms and Data Structures**, University of Oslo.

Assignment instructions, starter material and supporting datasets were provided by the course. Individual folders contain the source files, submissions and documentation associated with the exercises.
