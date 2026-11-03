# Assignment 4 — Sets with Hashing

A Java hashing exercise implementing a set with insertion, removal, membership checks and size lookup.

Completed for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**. This assignment was optional.

## Overview

The assignment requires a hash-based set supporting four operations:

| Operation | Behaviour |
| --- | --- |
| `contains x` | Print `true` if the set contains `x`, otherwise `false` |
| `insert x` | Add `x` unless it is already present |
| `remove x` | Remove `x` if present |
| `size` | Print the number of elements in the set |

Duplicate insertions must not increase the size. Removing an element that is not present must leave the set unchanged.

The required performance is expected amortized constant time for membership checks, insertion and removal, with constant-time size lookup. These are assignment requirements, not independently verified performance guarantees for the archived code.

## Files

| File or folder | Description |
| --- | --- |
| [AapenHashing.java](./Oblig4/AapenHashing.java) | Hash-based set source code |
| [HashList.java](./Oblig4/HashList.java) | Supporting list class |
| [input/](./Oblig4/input/) | Example and test inputs |
| [output/](./Oblig4/output/) | Corresponding expected outputs |
| [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) | Assignment instructions |

## Folder Structure

```text
Oblig4/
├── README.md
├── oppgavebeskrivelse.pdf
└── Oblig4/
    ├── AapenHashing.java
    ├── AapenHashing.class
    ├── HashList.java
    ├── input/
    └── output/
```

The `.class` file is a compiled artifact. Recompile the Java sources rather than relying on the archived binary.

## Input and Output

Input is read from **standard input**.

The first line specifies the number of operations. Each subsequent line contains one command:

```text
contains x
insert x
remove x
size
```

Only `contains` and `size` produce output, written to **standard output**.

### Example Input

```text
9
insert 1
insert 2
insert 3
insert 1
contains 1
contains 0
remove 1
contains 1
size
```

### Expected Output

```text
true
false
false
2
```

## Compile and Run

A Java Development Kit (JDK) is required.

From this assignment folder:

```bash
cd Oblig4
javac AapenHashing.java HashList.java
java AapenHashing < input/example
```

Run a larger test:

```bash
java AapenHashing < input/input_1000
```

## Check the Results

Save the program's output and compare it with the corresponding expected output:

```bash
java AapenHashing < input/example > actual_example.txt
diff output/example actual_example.txt
```

For another dataset:

```bash
java AapenHashing < input/input_1000 > actual_1000.txt
diff output/output_1000 actual_1000.txt
```

On systems with `diff`, no output from the comparison means the files match.

## Documentation

See [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) for the complete requirements and input/output specification.

## Author and Attribution

**Author:** Frida Berge (`fridatbe`)

Assignment instructions and test material were provided by the course. This folder preserves the Java source files and supporting inputs and outputs.
