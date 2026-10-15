# Lab 9: Nested Types, Enums, Records, and the Object Contract

This lab covers several features that are easy to overlook but come up a lot in real code. Nested classes let you keep helper types close to where they're used. Enums give you type-safe constants with behaviour. Records cut out the boilerplate for simple data carriers. And the Object contract (`equals`, `hashCode`, `toString`) explains why `HashSet` and `HashMap` can silently misbehave if you don't implement these methods consistently.

## What I practised
- The four kinds of nested class: static nested, inner, local, and anonymous
- Enums with fields and constant-specific method bodies
- Records as a concise alternative to value classes
- Overriding `equals`, `hashCode`, and `toString` correctly and consistently
- Understanding the contract between `equals` and `hashCode`

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab9` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.NestedDemo` | Program 9.1 — all four kinds of nested class in one place |
| `programs.EnumDemo` | Program 9.2 — enums with fields and constant-specific bodies |
| `programs.ObjectContract` | Program 9.3 — `equals`, `hashCode`, `toString`, and records |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.level.Level` | Basic 1: a `Level` enum with a `switch` expression giving advice per level |
| `exercises.record.RecordDemo` | Basic 2: a `record Student(name, age)` and what you get for free |
| `exercises.book.BookDemo` | Intermediate 1: `Book` with `equals`/`hashCode` based on ISBN — a `HashSet` correctly rejects duplicates |
| `exercises.linkedlist.LinkedListDemo` | Intermediate 2: a `LinkedList` built with a `private static Node` and an inner iterator class |
| `exercises.coin.Coin` | Challenge: a `Coin` enum and a `fewestCoins(amount)` greedy algorithm |

## Key takeaway

If two objects are `equal`, they must have the same `hashCode` — otherwise hash-based collections like `HashSet` and `HashMap` will silently store duplicates or lose entries. A `record` gives you a constructor, accessors, `equals`, `hashCode`, and `toString` all for free. A static nested class works without an instance of the outer class; an inner class always needs one.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
