# Lab 7: Exception Handling

Exceptions are Java's way of dealing with things that go wrong at runtime. This lab covers the full toolkit: catching exceptions, cleaning up with `finally`, throwing your own, declaring checked exceptions with `throws`, and managing resources safely with try-with-resources. There's also a tricky `finally` + `return` interaction worth understanding.

## What I practised
- `try` / `catch` / `finally` blocks and multi-catch
- The difference between checked and unchecked exceptions
- Throwing exceptions with `throw` and declaring them with `throws`
- Creating custom exception classes
- Cleaning up resources automatically with try-with-resources
- Exception chaining

## How to run

1. Open IntelliJ IDEA, go to **File > Open**, and select this `OOPLab7` folder.
2. If it asks for a Project SDK, choose JDK 17 or newer.
3. Open any class from the tables below and click the green arrow next to its `main` method.

## Programs from the manual

| Class | What it demonstrates |
|---|---|
| `programs.ExceptionBasics` | Program 7.1 — `try`, `catch`, `finally`, and multi-catch |
| `programs.Wallet` | Program 7.2 — a custom checked exception (`InsufficientFundsException`) |
| `programs.ResourceDemo` | Program 7.3 — try-with-resources and exception chaining |

## Exercises

| Class | What it demonstrates |
|---|---|
| `exercises.division.DivisionDemo` | Basic 1: Scanner-based division that handles bad input and divide-by-zero (interactive — type `q` to quit) |
| `exercises.array.ArrayAccess` | Basic 2: catching `ArrayIndexOutOfBoundsException` |
| `exercises.age.AgeValidator` | Intermediate 1: a checked `InvalidAgeException` that rejects ages outside 0–120 |
| `exercises.bank.BankDemo` | Intermediate 2: `BankAccount.withdraw` throwing `InsufficientFundsException` (design trade-offs discussed in `BankAccount.java`) |
| `exercises.finallydemo.FinallyReturn` | Challenge: `return` inside a `try` block when a `finally` block also runs — I predicted the output first, then verified it (explanation in the source) |

## Key takeaway

`finally` always runs when control leaves a `try` block, even if `return` is hit first (the return value is held while `finally` executes). Checked exceptions force callers to consciously handle errors — returning a boolean can be silently ignored. Try-with-resources closes resources in reverse order automatically, which is cleaner and safer than doing it in `finally`.

## Sample output

See `sample_output.txt` for the expected output of every `main` method in this lab.
