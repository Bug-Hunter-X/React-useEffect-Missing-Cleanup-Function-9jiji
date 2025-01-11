# React useEffect Missing Cleanup Function

This example demonstrates a common error in React's `useEffect` hook: omitting the cleanup function.  The `useEffect` hook, when used without a cleanup function, can lead to memory leaks or unexpected behavior, especially when dealing with subscriptions, timers, or event listeners.

The `bug.js` file shows the incorrect implementation, while `bugSolution.js` provides the corrected version.

## Bug:

The `useEffect` hook in `bug.js` logs 'Component mounted' when the component mounts, but lacks a cleanup function. This means that on component unmount, any side effects initiated within the effect will persist.

## Solution:

The `bugSolution.js` shows the corrected implementation.  The cleanup function ensures that any side effects are properly cleaned up when the component unmounts.  This prevents memory leaks and ensures predictable behavior.