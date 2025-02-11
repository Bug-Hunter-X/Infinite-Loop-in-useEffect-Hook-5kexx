# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by missing dependencies in the dependency array.

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log the current value of the `count` state variable. However, the dependency array is missing, causing the effect to run after every render, which leads to an infinite loop because updating the `count` triggers a re-render, and the effect runs again.

## Solution

The solution is to include `count` in the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` value changes.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Open your browser and observe the console for the infinite loop and high CPU usage.  Then, switch to the `bugSolution.js` file and observe the fixed version.
