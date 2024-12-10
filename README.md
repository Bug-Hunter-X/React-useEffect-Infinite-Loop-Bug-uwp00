# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The issue arises from an incomplete dependency array, causing an infinite render loop.

## Bug Description

The `useEffect` hook in `bug.js` is intended to log the current count. However, because `count` is missing from the dependency array, the effect is triggered on every render.  This results in a continuous update cycle and potentially a browser crash.

## Solution

The solution, shown in `bugSolution.js`, adds `count` to the dependency array of `useEffect`. This ensures the effect only runs when the `count` value changes.