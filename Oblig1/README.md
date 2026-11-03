```markdown
# Assignment 1 — Data Structures and Trees

Four exercises covering binary search trees, a triple-ended queue, tree traversal and insertion orders for balanced search trees.

Completed for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**.

## Overview

| Exercise | Topic | Folder |
| --- | --- | --- |
| 1 | Set operations using a binary search tree | [Oppgave1](./Oppgave1/) |
| 2 | Triple-ended queue (teque) | [Oppgave2](./Oppgave2/) |
| 3 | Finding a path from a tree node to the root | [Oppgave3](./Oppgave3/) |
| 4 | Generating insertion orders for balanced search trees | [Oppgave4](./Oppgave4/) |

For pseudocode, explanations and complexity analysis, see **[IN2010-innleveringsoppgave1.txt](./IN2010-innleveringsoppgave1.txt)**.

The full assignment instructions are available in [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf).

## Folder Structure

```text
Oblig1/
├── Oppgave1/
├── Oppgave2/
├── Oppgave3/
├── Oppgave4/
├── IN2010-innleveringsoppgave1.txt
├── oppgavebeskrivelse.pdf
└── README.md
```

## Exercise 1 — Set Operations

Implement a set using a binary search tree with the following operations:

- `contains x` — check whether an element exists.
- `insert x` — insert an element without introducing duplicates.
- `remove x` — remove an element if present.
- `size` — return the number of elements.

The assignment requires constant-time size lookup. The running time of the other operations depends on the tree's height; a balanced tree supports logarithmic-time search, insertion and removal.

[View exercise files →](./Oppgave1/)

## Exercise 2 — Teque

Implement a **triple-ended queue**, supporting insertion at the front, back and middle, together with indexed lookup.

Supported operations:

- `push_front x`
- `push_back x`
- `push_middle x`
- `get i`

Indices are zero-based. Each `get` operation prints the element at the requested position.

The written submission includes pseudocode and a running-time analysis.

[View exercise files →](./Oppgave2/)

## Exercise 3 — Kitten: Path to the Root

Given a tree and the node where a kitten is located, print the path from that node to the root.

The input describes parent–child relationships. The output lists the starting node followed by its ancestors, ending at the root.

This exercise is based on the Kattis problem [Kitten](https://open.kattis.com/problems/kitten).

[View exercise files →](./Oppgave3/)

## Exercise 4 — Balanced Search-Tree Insertion Order

Generate an ordering of distinct integers that produces a balanced binary search tree when inserted into an initially empty tree.

The exercise has two variants:

- **`balanserListe`** — work from a sorted list or array.
- **`balanserHeap`** — solve the same problem using heaps.

The task is to print a suitable insertion order, rather than implement the search tree itself.

[View exercise files →](./Oppgave4/)

## Input and Output

The programming exercises read from standard input and write to standard output. Input formats and examples are provided in the [assignment brief](./oppgavebeskrivelse.pdf).

## Documentation

See [IN2010-innleveringsoppgave1.txt](./IN2010-innleveringsoppgave1.txt) for the detailed written submission, including algorithm descriptions, pseudocode and analysis.

## Author and Attribution

**Author:** Frida Berge (`fridatbe`)

Assignment instructions were provided by the course. The teque and kitten exercises are based on Kattis problems.
```
