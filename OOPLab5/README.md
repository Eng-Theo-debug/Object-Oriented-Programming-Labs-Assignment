# Lab 5: Polymorphism

Polymorphism is what makes OOP genuinely flexible. This lab separates two concepts that are easy to confuse — overloading (resolved at compile time by argument types) and overriding (resolved at runtime by the actual object type). It also covers upcasting, dynamic dispatch, and how to safely downcast when you need to.

## What I practised
- Method overloading vs method overriding and when each applies
- Upcasting a subclass reference to a superclass type
- Dynamic dispatch — the JVM picks the right method based on the real object, not the declared type
- Safe downcasting with `instanceof` (including the modern pattern-matching syntax)
- Understanding that fields and static methods are *not* polymorphic

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab5` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.Calculator` | Program 5.1 — method overloading |
| `programs.Shapes` | Program 5.2 — method overriding and dynamic dispatch |
| `programs.CastingDemo` | Program 5.3 — casting, `instanceof` pattern matching, and why fields/static methods don't follow polymorphism |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.overload.PrintOverload` | Basic 1: `print()` overloaded for `int`, `double`, `String`, and `int[]` |
| `exercises.animals.AnimalDemo` | Basic 2: an `Animal[]` holding `Cat`, `Cow`, and `Duck` objects |
| `exercises.payroll.PayrollDemo` | Intermediate 1: adding an `Intern` subclass without touching the payroll loop |
| `exercises.fieldvsmethod.FieldVsMethod` | Intermediate 2: how methods, fields, and static members behave differently through a superclass reference (explained in the source) |
| `exercises.payment.PaymentDemo` | Challenge: comparing an `instanceof`-chain design against a clean polymorphic `process()` approach |

## Key takeaway

Overloading is a compile-time decision based on argument types. Overriding is a runtime decision based on the actual object. Fields and static methods always follow the declared reference type — they're not polymorphic. Polymorphic design means you can add a new subclass without editing any existing code that already works with the parent type.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
