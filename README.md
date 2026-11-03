# Algorithms and Data Structures

Coursework exploring trees, queues, sorting, graph algorithms and hashing for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**.

The repository contains source code, assignment briefs, datasets, test files and written submissions.

## Assignments

| Assignment | Topics | Documentation |
| --- | --- | --- |
| [Assignment 1](./Oblig1/) | Binary search trees, teque, tree paths and balanced insertion orders | [README](./Oblig1/README.md) |
| [Assignment 2](./Oblig2/) | Sorting algorithms, operation counting and performance experiments | [README](./Oblig2/README.md) |
| [Assignment 3](./Oblig3/) | IMDb graph construction, shortest paths, weighted paths and connected components | [README](./Oblig3/README.md) |
| [Assignment 4](./Oblig4/) | Hash-based sets, membership checks, insertion and removal | [README](./Oblig4/README.md) |

## Repository Structure

```text
algorithms-and-data-structures/
├── README.md
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
├── Oblig3/
│   ├── Actor and movie datasets
│   ├── Graph reference documents
│   ├── Hashing source files
│   └── oppgavebeskrivelse.pdf
└── Oblig4/
    ├── Oblig4/
    │   ├── Java source files
    │   ├── input/
    │   └── output/
    └── Assignment briefs
```

Each assignment has its own README with file descriptions and further instructions.

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

## Assignment 3 — Graph Algorithms with IMDb Data

The assignment explores an actor graph where movies connect actors who appeared together.

Tasks include:

- Constructing the graph from TSV files.
- Finding shortest paths between actors.
- Finding minimum-weight paths using movie ratings.
- Counting connected components by size.

The folder contains actor and movie datasets, smaller Marvel datasets, graph reference documents and hashing-related Java files. A runnable implementation of all graph tasks is not established by the available file listing.

[View Assignment 3 →](./Oblig3/)

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

See each assignment's README for its input format, source locations and available execution instructions.

## Documentation and Scope

This repository preserves coursework and supporting material rather than providing a single application or reusable algorithms library.

Assignment briefs describe the required tasks; they do not by themselves establish that every task is implemented. Written reports and archived results document the original submissions, not independently verified correctness or performance.

Compiled `.class` files can be regenerated from the Java sources.

## Dataset Usage

The IMDb-based dataset supplied for Assignment 3 is restricted to learning purposes according to the assignment brief. Consult that document and applicable IMDb terms before reuse.

## Author and Attribution

**Author:** Frida Berge (`fridatbe`)

Completed for **IN2010 — Algorithms and Data Structures**, University of Oslo.

Assignment instructions, starter material and supporting datasets were provided by the course. Individual folders contain the source files, submissions and documentation associated with the exercises.
