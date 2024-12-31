# React useEffect Infinite Loop Bug

This repository demonstrates a common issue in React applications involving the `useEffect` hook causing infinite re-renders.  The problem arises from logging the state variable within the `useEffect` without specifying a dependency array, resulting in an infinite loop.

## Problem
The provided `bug.js` file contains a React component that updates its state and logs the state value within the `useEffect` hook. This leads to an infinite render loop, as each state update causes the effect to run again and again.

## Solution
The solution (`bugSolution.js`) addresses this by adding a dependency array to the `useEffect` hook. The dependency array only runs the effect when the specified variables change, preventing the infinite loop.

## How to Reproduce
Clone the repo and run `npm start`.

## Note
This example is a simplified illustration of a real-world scenario.  Infinite loop issues in React frequently arise when dealing with complex state management and asynchronous operations within `useEffect` hooks.