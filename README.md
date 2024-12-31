# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The bug stems from a missing dependency in the `useEffect`'s dependency array, leading to an infinite re-render loop.  The solution shows how to correctly include the dependency to resolve the issue.

## Bug Description
The original `MyComponent` function uses `useEffect` without listing `count` in the dependency array.  This causes the effect to run on every render, changing the `count` state, triggering another render, and continuing the cycle.

## Solution
The solution adds `count` to the dependency array. Now, the `useEffect` runs only when the `count` value changes, preventing the infinite loop.