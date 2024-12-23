# Stale Closure in React's useEffect with setInterval

This repository demonstrates a common error in React applications involving stale closures within the `useEffect` hook when using `setInterval`.  The problem arises because the callback function within `setInterval` captures the value of `count` from the initial render, not the updated value in subsequent renders.

## Bug Description

The provided `bug.js` demonstrates an implementation where `setInterval` is used incorrectly within a `useEffect` hook. This results in the counter incrementing incorrectly or not at all. 

## Solution

The `bugSolution.js` demonstrates the correct implementation which updates the state value inside useEffect.  This avoids stale closure issues by utilizing the functional update pattern provided by the `setCount` function.