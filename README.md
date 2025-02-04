# Unnecessary useEffect re-renders in React 19

This repository demonstrates a common performance issue in React applications: an `useEffect` hook that runs after every render due to missing dependencies.  Improper use of `useEffect` can lead to wasted computation and unexpected side effects.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides the corrected implementation.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the component's behavior.  Note the frequent console logs in the `bug.js` version.

## Solution

The key is to specify the correct dependencies in the `useEffect` array.  In the corrected version (`bugSolution.js`), the effect only runs when the `count` state variable changes.