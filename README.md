# React useEffect Hook Missing Return Statement
This repository demonstrates a common React bug: a missing `return` statement in the `useEffect` hook.  This can lead to memory leaks and unexpected behavior, particularly when the effect performs cleanup actions (e.g., subscriptions, timers).

## Bug
The `bug.js` file contains a `MyComponent` that increments a counter.  The `useEffect` hook logs the count whenever it changes, but it's missing a return statement for cleanup. This leads to an infinite loop of updates.

## Solution
The `bugSolution.js` file fixes the issue by adding a return statement to the `useEffect` hook.  This ensures proper cleanup when the component unmounts or when the dependency array changes.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`
3. Run `npm start` (ensure you have a suitable React development environment set up)
4. Observe the infinite rendering or console errors.