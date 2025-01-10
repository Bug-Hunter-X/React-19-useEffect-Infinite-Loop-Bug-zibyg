# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common error in React 19's `useEffect` hook: an infinite loop caused by omitting state variables from the dependency array.

## Bug Description
The `useEffect` hook is designed to perform side effects after a component renders. If a state variable is used within the `useEffect` but not included in the dependency array, the effect runs on every render, leading to an infinite loop. This is because the effect function always has different values, triggering an infinite render loop. 

## Bug Reproduction
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the browser's console. 

## Solution
The solution is to include all state variables that are used within the `useEffect` function in its dependency array. This ensures that the effect only runs when those variables change.
