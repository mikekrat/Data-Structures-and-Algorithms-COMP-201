# Data Structures and Algorithms — COMP-201 (TUC)

Three Java projects for the Data Structures and Algorithms course (2019–2020),
each implementing a core data structure from scratch and benchmarking it on
generated datasets. **Grades: 9.3 / 10 / 9.7.**

## Projects

### Project 1 — Doubly linked list (text editor)
A line-based text editor backed by a hand-written **doubly linked list**.
Supports insert, delete, move and search over the lines of a file, with the
list exposed through a small editor API. Tested on input files scaled from a few
lines up to 1,000× to check that operations stay correct and responsive as the
document grows.

### Project 2 — Binary search trees (array vs. dynamic)
Two implementations of a **binary search tree** behind one common interface:
one backed by an array, one by dynamically allocated nodes. Both are measured on
sorted binary inputs from 50 up to 1,000,000 keys, comparing insertion, search
and traversal cost and the trade-offs between the contiguous-array and
pointer-based layouts.

### Project 3 — Linear hashing
A **linear hashing** table (dynamic, bucket-based hashing that grows one bucket
at a time) compared against the dynamic BST from Project 2 on the same key sets.
Shows how linear hashing keeps load factor and bucket chains bounded as the table
expands, and when hashing wins over a tree.

## Layout
```
PROJECT_1/  doubly linked list + text editor, with test files
PROJECT_2/  array BST and dynamic BST, with binary test datasets
PROJECT_3/  linear hashing vs. dynamic BST
```
Each project folder contains the Java sources (`src/`), the compiled classes
(`bin/`), the datasets used, and the assignment brief. Measurements and plots are
in the `ΠΙΝΑΚΑΚΙ – ΔΙΑΓΡΑΜΜΑΤΑ` (tables & charts) PDFs.

## Build & run
```bash
cd PROJECT_1/PLH202PROJECT1
javac -d bin src/*.java
java -cp bin MyEditor        # entry point differs per project (e.g. LinearMain in Project 3)
```

## Tech
Java · doubly linked lists · binary search trees · linear hashing · empirical
complexity analysis
