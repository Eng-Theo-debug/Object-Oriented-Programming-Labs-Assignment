# Lab 10: File I/O, Lambdas, and Streams

This lab brings together three things that work really well together in modern Java: reading and writing files with `java.nio.file`, expressing short behaviours inline with lambdas and method references, and processing collections with stream pipelines. The stream exercises in particular show how much cleaner data transformations can be compared to manual loops.

## What I practised
- Reading and writing text files using `Files` from `java.nio.file`
- CSV persistence — reading structured data from a file and writing it back
- Writing lambdas and method references for functional interfaces
- Building stream pipelines: `filter`, `map`, `sorted`, `collect`, `groupingBy`
- Understanding that streams are lazy and cannot be reused after a terminal operation

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab10` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.
4. File paths are relative to the project root — that's the default working directory in IntelliJ.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.FileDemo` | Program 10.1 — reading and writing text files (creates `students.txt`) |
| `programs.StudentRepository` | Program 10.2 — CSV persistence (creates `learners.csv`) |
| `programs.StreamDemo` | Program 10.3 — lambdas, method references, and stream pipelines |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.userlines.UserLines` | Basic 1: saves 5 user-typed lines to a file and reads them back (interactive) |
| `exercises.removeeven.RemoveEven` | Basic 2: using a `Predicate` with `removeIf` to delete even numbers from a list |
| `exercises.textstats.TextStats` | Intermediate 1: counts lines, words, and characters in a file (defaults to `sample.txt`; pass a path as a program argument to use another file) |
| `exercises.average.AboveAverage` | Intermediate 2: filters students above the class average and sorts them alphabetically |
| `exercises.bands.GradeBands` | Challenge: groups students from `learners.csv` into bands A/B/C and writes `report_A.txt`, `report_B.txt`, and `report_C.txt` |

## Key takeaway

File operations throw checked `IOException`, so you have to handle or declare it — no ignoring it by accident. Relative paths resolve against the working directory, which in IntelliJ defaults to the project root. Streams are lazy: nothing runs until a terminal operation (like `collect` or `forEach`) is called, and once a stream is consumed it can't be reused.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.

> Note: Running Programs 10.1 and 10.2 will create `students.txt` and `learners.csv` in the project folder.
