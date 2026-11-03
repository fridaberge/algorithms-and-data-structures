# Assignment 3 — Hashing

Java source files for an open-hashing exercise, accompanied by actor and movie datasets and graph reference documents.

Completed for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**.

## Overview

The folder contains:

- An open-hashing implementation.
- A supporting list class.
- Notes on changes to insertion and removal.
- Actor and movie datasets in TSV format.
- Two Marvel graph documents.

See [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) for the full assignment requirements.

## Files

| File | Description |
| --- | --- |
| [AapenHashing.java](./AapenHashing.java) | Open-hashing source code |
| [HashList.java](./HashList.java) | Supporting list class |
| [actors.tsv](./actors.tsv) | Actor dataset |
| [movies.tsv](./movies.tsv) | Movie dataset |
| [marvel_actors.tsv](./marvel_actors.tsv) | Marvel actor dataset |
| [marvel_movies.tsv](./marvel_movies.tsv) | Marvel movie dataset |
| [marvelgraph_labeled.pdf](./marvelgraph_labeled.pdf) | Labeled Marvel graph document |
| [marvelgraph_nodetypes.pdf](./marvelgraph_nodetypes.pdf) | Alternative Marvel graph document |
| [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) | Original assignment instructions |

## Hashing

Open hashing, also called separate chaining, handles collisions by storing multiple elements in a bucket associated with a table index.

The source files cover the hash-table implementation and its supporting list structure.

## Recorded Code Changes

The original README documents changes at lines **84, 126 and 130**, referring to the source version at the time.

The changes use direct access to the table's bucket when:

- Adding an element: `h.liste[i].liste.add(tall)`
- Clearing a bucket: `h.liste[i] = null`
- Removing an element: `h.liste[i].liste.remove(tall)`

### Java Reference Clarification

The original notes describe `b` as a copy. In Java, assigning an object reference to another variable does **not** copy the object.

If `b` refers to the same bucket as `h.liste[i]`, modifying `b.liste` also modifies that shared bucket. However, assigning `b = null` only changes the local variable—it does not clear the table entry. Clearing that entry requires `h.liste[i] = null`.

Whether the list-operation changes were necessary depends on how `b` was initialized in the surrounding code.

## Datasets and Graph Documents

The TSV files contain actor and movie data, including Marvel-specific datasets. The PDF files provide accompanying graph documents.

Consult the assignment brief for their intended use, input formats and required tasks.

## Documentation

**[Read the assignment brief →](./oppgavebeskrivelse.pdf)**

## Author and Attribution

**Author:** Frida Berge (`fridatbe`)

Assignment instructions and supporting material were provided by the course. This folder preserves the source files and modification notes associated with the exercise.
