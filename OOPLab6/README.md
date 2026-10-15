# Lab 6: Abstraction, Abstract Classes, and Interfaces

Abstraction is about defining *what* something should do without committing to *how* it does it. This lab covers two tools for that: abstract classes (for closely related types that share some common code) and interfaces (for capabilities that can be bolted onto unrelated types). It also introduces `Comparable` and `Comparator` for sorting.

## What I practised
- Defining abstract classes and abstract methods
- Writing interfaces with default and static methods
- Deciding when to use an abstract class vs an interface
- Implementing `Comparable` and using `Comparator` for custom sorting
- Resolving conflicting default methods from multiple interfaces

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab6` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.VehicleDemo` | Program 6.1 — abstract class with a concrete and an abstract method |
| `programs.InterfaceDemo` | Program 6.2 — interfaces, `default`/`static` methods, and multiple interface implementation |
| `programs.ComparableDemo` | Program 6.3 — implementing `Comparable<T>` for natural ordering |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.shape.ShapeDemo` | Basic 1: abstract `Shape`; concrete `Circle`, `Rectangle`, and `Square` |
| `exercises.flyable.FlyableDemo` | Basic 2: a `Flyable` interface shared by the unrelated `Bird` and `Aeroplane` classes |
| `exercises.account.AccountDemo` | Intermediate 1: abstract `Account` with an abstract `monthlyFee()` for each account type to define |
| `exercises.student.StudentDemo` | Intermediate 2: `Comparable` by name, plus a `Comparator` by marks |
| `exercises.diamond.DiamondDemo` | Challenge: two interfaces provide the same `default` method — resolved with `InterfaceName.super.hello()` (the rule is explained in the source) |

## Key takeaway

Use an abstract class when closely related classes share actual code or state. Use an interface when you want to give an unrelated group of classes the same capability. If two interfaces provide the same default method and a class implements both, the class must override it — and can pick one parent's version using `X.super.method()`.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
