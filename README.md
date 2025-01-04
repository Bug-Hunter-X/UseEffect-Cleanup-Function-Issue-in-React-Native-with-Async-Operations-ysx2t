# React Native useEffect Cleanup Issue with Async Operations

This repository demonstrates a common issue encountered when using the `useEffect` hook in React Native with asynchronous operations. The problem arises when the component unmounts before the asynchronous operation inside the `useEffect` hook completes, preventing the cleanup function from executing as expected.

This can lead to several issues, including:

* Memory leaks: If the asynchronous operation holds references to the component or its state, these resources may not be released until the cleanup function executes.
* Unexpected state changes: The asynchronous operation might still update state after the component unmounts, leading to unexpected behavior in other parts of the application.

This example showcases the issue and provides a solution to address it.