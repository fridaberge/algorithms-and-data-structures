# Assignment 3 — Graph Algorithms with IMDb Data

An assignment covering graph construction, shortest paths, weighted paths and connected components using actor and movie data.

Completed for **IN2010 — Algorithms and Data Structures** at the **University of Oslo**.

## Overview

| Exercise | Topic |
| --- | --- |
| 1 | Build a graph from actor and movie datasets |
| 2 | Find shortest paths between actors |
| 3 | Find minimum-weight paths based on movie ratings |
| 4 | Count connected components by size |
| 5 | Optional exploration of the dataset |

See [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) for the full requirements and example outputs.

This README describes the assignment and the available files. It does not claim that all graph exercises are implemented in the archived source.

## Files

| File | Description |
| --- | --- |
| [actors.tsv](./actors.tsv) | Actor identifiers, names and associated movie identifiers |
| [movies.tsv](./movies.tsv) | Movie identifiers, titles, ratings and vote counts |
| [marvel_actors.tsv](./marvel_actors.tsv) | Smaller actor dataset for testing |
| [marvel_movies.tsv](./marvel_movies.tsv) | Smaller movie dataset for testing |
| [marvelgraph_labeled.pdf](./marvelgraph_labeled.pdf) | Labeled Marvel graph reference |
| [marvelgraph_nodetypes.pdf](./marvelgraph_nodetypes.pdf) | Alternative Marvel graph reference |
| [AapenHashing.java](./AapenHashing.java) | Hashing source retained in this folder |
| [HashList.java](./HashList.java) | Supporting list class |
| [oppgavebeskrivelse.pdf](./oppgavebeskrivelse.pdf) | Original assignment instructions |

The listed Java files concern hashing; their presence alone does not establish an implementation of the IMDb graph tasks.

## Dataset and Graph Model

The assignment uses two tab-separated files.

### Movies

Each line of `movies.tsv` contains:

```text
movie_id    title    rating    vote_count
```

Movies are identified by IMDb `tt` identifiers. Ratings range from 0 to 10. Vote counts are not required for the main exercises.

### Actors

Each line of `actors.tsv` contains:

```text
actor_id    name    movie_id_1    movie_id_2    ...
```

Actors are identified by IMDb `nm` identifiers.

Movie references that do not appear in `movies.tsv` must be ignored.

### Graph Representation

The main graph is an **undirected multigraph**:

- Nodes represent actors.
- An edge connects two actors who appeared in the same movie.
- Edges carry the movie's title and rating.
- Multiple shared movies can produce parallel edges between the same actors.

The assignment also permits an alternative representation with actor and movie nodes, where edges connect actors to their movies.

The smaller Marvel datasets provide a convenient starting point before processing the full dataset.

## Exercise 1 — Build the Graph

Read the actor and movie files and construct a suitable graph representation.

Print the number of nodes and edges as a basic consistency check.

The assignment gives these reference counts for its actor-based graph:

| Measure | Reference value |
| --- | --- |
| Nodes | 119,205 |
| Edges | 5,068,918 |

Other valid representations may produce different counts. Any differences should be explained in the written submission.

## Exercise 2 — Six Degrees of IMDb

Find a shortest path between two actors, minimizing the number of actor-to-actor connections.

Print the actors along the path and the movies connecting them. Multiple shortest paths are acceptable.

The required actor pairs are:

| Starting actor | Destination actor |
| --- | --- |
| Donald Glover | Jeremy Irons |
| Scarlett Johansson | Denzel Washington |
| Carrie Coon | Julie Delpy |
| Christian Bale | Angelina Jolie |
| Atle Antonsen | Michael K. Williams |

For the actor-based graph, breadth-first search is a suitable approach because each connection counts as one step.

## Exercise 3 — “Chillest” Path

Find a path that favours highly rated movies rather than simply minimizing the number of connections.

The assignment defines the weight of a movie edge as:

\[
w = 10 - r
\]

where \(r\) is the movie's rating.

A higher rating therefore gives a lower edge weight. The goal is to minimize the total weight along the path.

Use the same actor pairs as in Exercise 2, and print:

- The actors on the path.
- The connecting movies and their ratings.
- The total path weight.

Dijkstra's algorithm is suitable for this weighting because all edge weights are non-negative.

## Exercise 4 — Connected Components

Find the graph's connected components and group them by size.

The output should report how many components contain each number of nodes, for example:

```text
There are 2 components of size 10
There are 4 components of size 9
```

A traversal such as breadth-first or depth-first search can identify each component by visiting all nodes reachable from an unvisited starting node.

## Exercise 5 — Optional Exploration

The bonus exercise invites additional questions about the dataset, such as:

- When does a shortest path differ substantially from a minimum-weight path?
- Could another weighting function make use of vote counts?
- How many movies are needed to preserve the largest connected component?

See the assignment brief for the complete suggestions.

## Running and Documentation

The assignment specifies a runnable program with an entry point named:

- `Innleveringsoppgave3.java` for Java, or
- `innleveringsoppgave3.py` for Python.

These entry-point files are not shown in the available folder listing, so no verified run command is documented here.

The required written submission should explain how to run the program, which algorithms were used and any known limitations.

## Dataset Usage

The assignment states that the supplied dataset is for learning purposes only and must not be used for other purposes. Consult the assignment brief and applicable IMDb terms before reusing it.

## Author and Attribution

**Author:** Frida Berge (`fridatbe`)

Assignment instructions and supporting datasets were provided by the course. The actor and movie data is based on IMDb.
