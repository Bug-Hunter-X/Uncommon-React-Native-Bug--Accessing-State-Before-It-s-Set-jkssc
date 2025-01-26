# Uncommon React Native Bug: Accessing State Before It's Set

This repository demonstrates a common yet often overlooked bug in React Native: accessing state variables or props before they've been properly initialized.  This usually manifests during asynchronous operations like data fetching.

## The Bug

The `bug.js` file illustrates the problem. The component attempts to render data from the state before the asynchronous operation to fetch it has completed. This often results in `undefined` or `null` values being accessed, leading to crashes or unexpected behavior.

## The Solution

The `bugSolution.js` file demonstrates a solution using the `useEffect` hook and conditional rendering.  We only attempt to render the data once the asynchronous operation is complete and the state has been updated.