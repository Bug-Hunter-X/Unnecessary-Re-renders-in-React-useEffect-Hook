# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook where unnecessary re-renders occur due to an incorrect dependency array. The component re-renders even when the state value doesn't change. 

The `bug.js` file contains the buggy code and `bugSolution.js` file has the corrected code.

## Problem

The `useEffect` hook in the original code doesn't effectively check for changes in the state variable `count`. It triggers on every state update, regardless of whether there's an actual change in the value. This leads to unnecessary re-renders and performance degradation.

## Solution

The solution in `bugSolution.js` shows the correct way to use useEffect to only perform an action when count changes.  This ensures that the effect is triggered only when the value of `count` changes, improving performance and avoiding unnecessary re-renders.