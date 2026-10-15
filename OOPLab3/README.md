# Lab 3: Encapsulation and Access Modifiers

Encapsulation is about protecting an object's internal state so it can only be changed in controlled, predictable ways. This lab covers making fields `private`, validating data in setters and constructors, and avoiding the subtle bug where returning a reference to an internal mutable object lets outside code break your class's invariants.

## What I practised
- Hiding fields with `private` and exposing them through getters/setters
- Validating input in setters and constructors
- Avoiding mutable reference leaks (defensive copies)
- Building a fully immutable class

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab3` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.BankDemo` | Program 3.1 — a safe `BankAccount` that validates every deposit and withdrawal |
| `programs.Team` | Program 3.2 — the defensive-copy trap: what happens when a getter returns an internal list directly |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.student.StudentDemo` | Basic 1–2: Student with marks validated to 0–100 and a derived `getGrade()` method |
| `exercises.history.HistoryDemo` | Intermediate 1: BankAccount that keeps a transaction history; the getter returns an unmodifiable copy |
| `exercises.immutable.ImmutablePersonDemo` | Intermediate 2: a fully immutable Person class — every design decision is explained in the source |
| `exercises.temperature.TemperatureDemo` | Challenge: Temperature stored in Kelvin; rejects any value below absolute zero |

## Key takeaway

`private` fields plus validated constructors and setters keep objects in a consistent, valid state at all times. Getters must never return a reference to an internal mutable object — wrap it in an unmodifiable view or return a copy instead. An immutable class should be `final`, have `private final` fields, no setters, and defensive copies in any constructor that accepts mutable objects.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
