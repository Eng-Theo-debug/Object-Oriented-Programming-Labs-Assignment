# Lab 8: Generics and the Collections Framework

Before generics, you'd write a container class that accepted `Object` and then cast everything back out — with no safety net. This lab shows how generics move type errors to compile time, and covers the main collection types in the Java standard library: `List`, `Set`, `Map`, and `Deque`.

## What I practised
- Writing generic classes and methods with type parameters
- Bounded type parameters (`<T extends Comparable<T>>`)
- Choosing the right collection for the job: `List`, `Set`, `Map`, `Deque`
- Sorting with `Comparable` and `Comparator`
- Why generics only work with reference types (no primitives)

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab8` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.GenericsDemo` | Program 8.1 — `Box<T>`, `Pair<K,V>`, and generic methods |
| `programs.CollectionsDemo` | Program 8.2 — `List`, `Set`, `Map`, and `Deque` in action |
| `programs.SortingDemo` | Program 8.3 — `Comparable` and `Comparator` for sorting |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.numbers.NumberList` | Basic 1: 10 integers — sum, maximum, and reversed |
| `exercises.duplicates.RemoveDuplicates` | Basic 2: removing duplicates using a `Set` |
| `exercises.stack.StackDemo` | Intermediate 1: a generic `Stack<T>` backed by an `ArrayList` |
| `exercises.wordfreq.WordFrequency` | Intermediate 2: word frequencies sorted by count, descending |
| `exercises.sort.BubbleSort` | Challenge: a generic `bubbleSort(T[])` method — and an explanation of why `int[]` doesn't work with it |

## Key takeaway

Generics catch type mistakes at compile time instead of at runtime. They only work with reference types, which is why you use `Integer[]` instead of `int[]`. When picking a collection: use `List` when order and duplicates matter, `Set` for uniqueness, `Map` for key-value lookup, and `Deque` when you need stack or queue behaviour.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
