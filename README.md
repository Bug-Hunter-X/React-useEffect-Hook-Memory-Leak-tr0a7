# React useEffect Hook Memory Leak

This example demonstrates a common mistake in React's `useEffect` hook: forgetting to include a cleanup function to prevent memory leaks.  Specifically, a `setInterval` is started without being stopped when the component unmounts.

## Bug
The `bug.js` file contains the flawed code.  The `setInterval` runs continuously, even after the component is unmounted, leading to a memory leak.

## Solution
The `bugSolution.js` file provides the corrected code.  The cleanup function clears the interval when the component unmounts, preventing the memory leak.