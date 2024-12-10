# React useEffect setInterval Memory Leak
This example demonstrates a common error in React where `setInterval` is used within the `useEffect` hook without proper cleanup. This leads to a memory leak as the interval continues to run even after the component unmounts.

The `bug.js` file contains the problematic code, and `bugSolution.js` provides the corrected version.

## Problem
The `setInterval` function, when used within `useEffect` without a return function for cleanup, keeps running even after the component is unmounted. This causes a memory leak as the interval continues to allocate resources.

## Solution
The solution is to use the return value of `useEffect` to add a cleanup function. This function clears the interval when the component unmounts, preventing the memory leak.

This is crucial for preventing memory leaks and ensures your React application runs smoothly.