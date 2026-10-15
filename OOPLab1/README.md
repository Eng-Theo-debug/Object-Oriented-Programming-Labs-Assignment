# Lab 1: Classes and Objects

This first lab is all about getting comfortable with the basic building blocks of OOP — classes, objects, and references. The exercises cover creating classes with fields and methods, building objects with `new`, and understanding what it actually means when two variables point to the same object.

## What I practised
- Defining a class with fields and methods
- Creating objects with `new` and accessing members with the dot operator
- Understanding references, aliasing, and `null`

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab1` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.Student` | Program 1.1 — Student class with fields, `display()`, and `isHonours()` |
| `programs.ReferenceDemo` | Program 1.2 — references, aliasing, `==` vs `equals`, and `null` |
| `programs.Course` | Program 1.3 — an object that holds a reference to another object |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.car.CarDemo` | Basic 1–2: Car class with `brand`, `year`, `mileage`, `display()`, and `isAntique()` |
| `exercises.rectangle.RectangleDemo` | Intermediate 1–2: finds the largest of 5 rectangles; the aliasing prediction (`r2 = r1`) is explained in the source comments |
| `exercises.person.PersonDemo` | Challenge: Person holds an Address; shows chained dot expressions and the `NullPointerException` risk |

## Key takeaway

An object variable stores a reference, not the object itself. So writing `Rectangle r2 = r1;` makes both variables point to the same object — changing `r2.width` also changes `r1.width`. Chaining dots on a `null` reference throws a `NullPointerException`, so always check for `null` first.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
