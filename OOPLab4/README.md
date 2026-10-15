# Lab 4: Inheritance

Inheritance lets one class build on top of another, reusing and extending its behaviour. This lab covers the mechanics — the `extends` keyword, calling `super`, the order constructors run across a hierarchy — and also addresses the important design question of when inheritance is actually the right choice vs when composition is better.

## What I practised
- Creating subclasses with `extends` and using `super` to call parent constructors and methods
- Understanding the constructor call chain across multiple levels
- Using `final` to prevent further subclassing
- Recognising when composition is a better fit than inheritance

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab4` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.CompanyDemo` | Program 4.1 — Employee / Manager / Developer hierarchy |
| `programs.Chain` | Program 4.2 — constructor call order traced through three levels of inheritance |
| `programs.CompositionDemo` | Program 4.3 — a `final` class, overriding `toString`, and a composition example |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.person.PersonDemo` | Basic 1–2: Person, Student, and Teacher sharing a single `display()` method |
| `exercises.vehicle.VehicleDemo` | Intermediate 1: Vehicle → Car → ElectricCar, with constructor call order traced |
| `exercises.noargs.NoArgsDemo` | Intermediate 2: why `Dog extends Animal` fails if the superclass has no no-arg constructor (explained in `Animal.java`) |
| `exercises.stack.StackDemo` | Challenge: Stack implemented via inheritance (`BadStack`) vs composition (`GoodStack`) — with a comparison of both approaches |

## Key takeaway

Superclass constructors always run before the subclass body. If the superclass doesn't have a no-argument constructor, the subclass must explicitly call `super(...)` as its first line. The inheritance vs composition question is a real design decision — a Stack *has* a list, it is not a list, so composition is the cleaner fit.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
