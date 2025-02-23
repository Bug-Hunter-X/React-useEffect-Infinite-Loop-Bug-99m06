# React useEffect Infinite Loop
This example demonstrates a common error in React's `useEffect` hook: creating an infinite loop by incorrectly specifying the dependency array.

The `bug.js` file shows the problematic code, where the `useEffect` hook's dependency array includes the `count` state variable.  This causes the effect to run every time `count` changes, resulting in an infinite loop as `setCount` is called inside the effect.

The `bugSolution.js` file provides a corrected version, demonstrating the correct way to handle this situation using `useRef`. 