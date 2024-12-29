# React useEffect setInterval Memory Leak
This example demonstrates a common error in React components: using `setInterval` within `useEffect` without providing a cleanup function. This leads to memory leaks because the interval continues to run even after the component unmounts.

## Bug
The `bug.js` file shows a component that increments a counter every second using `setInterval`. However, it lacks a cleanup function in `useEffect` to clear the interval when the component unmounts.

## Solution
The `bugSolution.js` file demonstrates the correct implementation, including a cleanup function to clear the interval before the component is unmounted. This prevents the memory leak.
