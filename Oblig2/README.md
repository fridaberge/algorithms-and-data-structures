# Assignment 2 — Sorting Algorithms and Performance

Implementation and experimental comparison of four sorting algorithms in Java.

Completed for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**.

## Overview

The assignment consists of three parts:

1. **Correctness:** sort input files and inspect the resulting output.
2. **Measurement:** record comparisons, swaps and execution time.
3. **Experiments:** compare the algorithms across input sizes and input orderings.

For the experiment descriptions, findings and charts, see **[IN2010-innlevering2.pdf](./Oblig2/IN2010-innlevering2.pdf)**.

The full instructions are available in [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf).

## Sorting Algorithms

| Algorithm | Typical time complexity | Worst-case time complexity | Source |
| --- | --- | --- | --- |
| Insertion sort | Input-dependent; efficient on nearly sorted data | Quadratic | [Insertion.java](./Oblig2/Insertion.java) |
| Selection sort | Quadratic | Quadratic | [Selection.java](./Oblig2/Selection.java) |
| Quicksort | Linearithmic on average | Quadratic | [Quick.java](./Oblig2/Quick.java) |
| Merge sort | Linearithmic | Linearithmic | [Merge.java](./Oblig2/Merge.java) |

Insertion sort and quicksort were required. Selection sort and merge sort were chosen as the two additional algorithms.

## Folder Structure

```text
Oblig2/
├── README.md
├── oppgavebeskrivelse.pdf
└── Oblig2/
    ├── IN2010-innlevering2.pdf
    ├── Innlevering2.java
    ├── Innlevering2Runner.java
    ├── Insertion.java
    ├── Merge.java
    ├── Quick.java
    ├── Selection.java
    ├── Sorter.java
    ├── oblig2.docx
    ├── README.md
    └── innlevering2_h22_src-master/
        ├── README.md
        ├── example
        └── inputs/
```

## Part 1 — Correctness

Each algorithm sorts integers into ascending order.

The submitted report documents testing all four algorithms with:

- `nearly_sorted_10`
- `random_10`

These small inputs were chosen so the sorted results could be checked visually.

The assignment specifies one output file per algorithm, named using the input filename and algorithm name:

```text
example_insertion.out
example_selection.out
example_quick.out
example_merge.out
```

Each output file contains one integer per line.

## Part 2 — Comparisons, Swaps and Time

The measurement framework records:

- Number of comparisons.
- Number of swaps or counted data movements.
- Sorting time in microseconds.

For an input containing a given number of integers, the assignment measures every prefix, starting with the empty array and ending with the complete input.

Results are written to a CSV file:

```text
<input_filename>_results.csv
```

For each algorithm, the CSV includes columns following this pattern:

```text
<algorithm>_cmp, <algorithm>_swaps, <algorithm>_time
```

### Counting Conventions

The report describes using comparison and swap methods from `Sorter.java` to update the counters.

Two conventions are important when interpreting the results:

- Comparison counts include instrumented loop and condition checks, not only comparisons between array elements.
- Merge sort counts writes back to the original array as swaps, although these are not pairwise exchanges.

The counters therefore reflect the implementation's measurement choices and should not be treated as identical operations across all algorithms.

## Part 3 — Experiments

The experiments compare random and nearly sorted inputs of different sizes.

The workflow described in the report was:

1. Compile and run the Java programs with selected input files.
2. Import the generated CSV data into Excel.
3. Create charts for execution time, comparisons and swaps.
4. Compare the observed behaviour of the algorithms.

The report discusses small-input overhead, performance on larger inputs and insertion sort's effectiveness on nearly sorted data.

These are observations from the recorded experiments, rather than universal performance guarantees. Timing also depends on the implementation and execution environment.

**[Read the report and view the charts →](./Oblig2/IN2010-innlevering2.pdf)**

## Input Files

Input consists of non-negative integers, one per line. The input filename is supplied as a command-line argument.

The provided datasets include:

- **Nearly sorted** inputs.
- **Random** inputs.
- Sizes ranging from **10 to 1,000,000 elements**.

[Browse the datasets →](./Oblig2/innlevering2_h22_src-master/inputs/)

Running every prefix with quadratic-time algorithms can be expensive on large datasets. The assignment recommends selecting the faster algorithms for larger experiments.

## Building

From this assignment folder, compile the Java sources:

```bash
cd Oblig2
javac *.java
```

See the [source-folder README](./Oblig2/README.md) and the entry-point classes for the available execution commands and experiment configuration.

## Documentation

| Document | Contents |
| --- | --- |
| [IN2010-innlevering2.pdf](./Oblig2/IN2010-innlevering2.pdf) | Submitted report, measurement conventions, experiment discussion and charts |
| [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) | Original assignment instructions |
| [Starter-material README](./Oblig2/innlevering2_h22_src-master/README.md) | Documentation included with the supplied framework |

## Author and Attribution

**Author:** Frida Berge  
**Report date:** 12 October 2022

Assignment instructions, the measurement framework and input datasets were supplied by the course. The submission implements the sorting algorithms and documents the experiments.
