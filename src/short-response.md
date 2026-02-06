# Short Response Questions

## Question 1: Promise States

What are the three states of a Promise? For each state, explain what it represents and which Promise method (`.then()` or `.catch()`) is used to handle it.

The three states of a promise are: pending, resolved, rejected. The _pending_ state means that the operation is still in process. The _resolved_ state represents the fulfillment of the promise, meaning that the operation was successful and is handled by `.then()`. The _rejected_ state represents the failure of the promise, it typically returns an error and is handled by `.catch()`.

## Question 2: Callback Hell vs. Promise Chaining

Explain why deeply nested callbacks (callback hell) are problematic, and describe how Promise chaining with `.then()` solves this problem.

Deeply nested callbacks are problematic because it can become **hard to read and maintain**. Promise chaining with `.then()` solves this problem by **invoking each step** as the promise resolves, allowing the code to be written in a **chronological order** and making it easier to read and maintain.

## Question 3: Error Handling with `.catch()`

If you have a chain of three `.then()` calls followed by a single `.catch()`, and the second `.then()` throws an error, what happens? Why is this behavior useful?

The `.catch()` is activated and handles the error. This behavior is useful because it allows errors thrown anywhere in the promise chain to be **caught in one place**, preventing the remaining `.then()` calls from executing.
