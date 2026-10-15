# Lab 11: Design Patterns and the Mini-Project

The final lab ties everything together. The first part introduces four classic design patterns — Singleton, Factory, Strategy, and Observer — with focused demos for each. The second part is the mini-project: a fully working Library Management System that uses abstract classes, interfaces, polymorphism, custom exceptions, collections, streams, and CSV file persistence all at once.

## What I practised
- Singleton pattern — ensuring only one instance of a class exists
- Factory pattern — delegating object creation to a dedicated method
- Strategy pattern — swapping algorithms at runtime without changing the caller
- Observer pattern — notifying interested objects when state changes
- SOLID-style design: single responsibility, open for extension
- Integrating multiple OOP concepts into one coherent application

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab11` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.SingletonFactoryDemo` | Program 11.1 — Singleton and Factory patterns |
| `programs.StrategyObserverDemo` | Program 11.2 — Strategy and Observer patterns |

## Mini-project — Library Management System

| Class | What it does |
|---|---|
| `library.LibraryApp` | Interactive menu-driven application — the main entry point for the mini-project |
| `library.LibraryDemo` | Scripted walkthrough of every requirement (non-interactive, good for a quick demo) |
| `library.LibraryTests` | 29 automated checks covering all the core functionality |

## Key takeaway

Design patterns are named, reusable solutions to common design problems — they give you and your teammates a shared vocabulary. The mini-project shows how everything from Labs 1–10 fits together: abstract classes and interfaces for the item hierarchy, polymorphism for borrowing behaviour, custom exceptions for domain-specific errors, `Map` and streams for data management, and CSV files for persistence.

## Extra documents

- `docs/ClassDiagram.md` — UML class diagram for the Library Management System
- `docs/REPORT.md` — short project report covering design decisions

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
