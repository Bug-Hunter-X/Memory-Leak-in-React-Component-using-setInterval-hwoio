# React setInterval Memory Leak
This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook: forgetting to clear the interval when the component unmounts. This results in a memory leak and potential performance issues.

## Problem
The `setInterval` function continues to update the state even after the component is unmounted, leading to memory leaks because the callback function still holds a reference to the component's state and other variables.  This is especially problematic in applications with many components using `setInterval`.