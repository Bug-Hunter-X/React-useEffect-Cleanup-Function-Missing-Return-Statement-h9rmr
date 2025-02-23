# React useEffect Cleanup Function Missing Return Statement

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  Specifically, it showcases a scenario where the cleanup function within `useEffect` is missing a `return` statement, leading to potential memory leaks and unexpected behavior.

## The Bug

The `bug.js` file contains a component that uses the `useEffect` hook to add an event listener.  However, the cleanup function, which is responsible for removing the event listener when the component unmounts or when dependencies change, is missing the crucial `return` statement. This omission prevents the removal of the event listener, potentially leading to memory leaks if the component is frequently mounted and unmounted.

## The Solution

The `bugSolution.js` file demonstrates the corrected version of the component.  The `return` statement has been added to the `useEffect` cleanup function, ensuring that the event listener is properly removed when necessary.

## How to Run

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`.

You can then observe the behavior of both the buggy and corrected versions of the component.