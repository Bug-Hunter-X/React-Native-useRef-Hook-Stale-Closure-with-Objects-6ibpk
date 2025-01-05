# React Native useRef Hook Stale Closure with Objects

This repository demonstrates a common yet subtle issue in React Native when using the `useRef` hook with object initial values.  Directly modifying the object's properties doesn't trigger re-renders, leading to stale closures.  The `bug.js` file shows the problematic code. The solution involves creating a new object or using a state management solution.

## Problem

The `useRef` hook is often used to store mutable values that don't trigger re-renders. However, when the initial value is an object and you modify its properties directly, React won't detect these changes because the reference itself remains the same.

## Solution

The `bugSolution.js` file offers a solution.  Instead of directly modifying the object, we create a new object with the updated value, effectively forcing a re-render because `myRef.current` now points to a new object.

## Setup

1. Clone this repository.
2.  Run `npm install` or `yarn install`.
3. Run the app on your preferred emulator or device.