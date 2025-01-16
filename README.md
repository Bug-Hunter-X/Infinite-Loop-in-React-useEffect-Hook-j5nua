# React useEffect Infinite Loop Bug

This repository demonstrates a common error when using the `useEffect` hook in React: creating an infinite loop by incorrectly specifying dependencies.

## Bug Description
The `useEffect` hook in `bug.js` has an incorrect dependency declaration.  It sets the `count` state inside the effect function, which causes a re-render.  Because `count` is in the dependency array, the effect runs again, creating an infinite loop. 

## Solution
The solution provided in `bugSolution.js` fixes the issue by removing `count` from the dependency array.  The effect will now only run once after the initial render.  Alternatively, one can introduce a conditional statement or add an additional dependency to control when the effect runs. 

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the infinite loop.