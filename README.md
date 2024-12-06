# React Native: useEffect Cleanup Function Throws Error After Unmount

This repository demonstrates a common error in React Native applications where a cleanup function within the `useEffect` hook throws an error after the component has unmounted.  The error typically occurs because the cleanup function attempts to access or modify the component's state or props after the component is no longer in the DOM.

## Problem

The `bug.js` file contains a React Native component that fetches data using `useEffect`. The cleanup function attempts to set state (`setData(null)`) even after the component has unmounted. This causes an error because the component's state no longer exists.

## Solution

The `bugSolution.js` file provides a solution to this issue. The solution checks if the component is still mounted before accessing/modifying state. This is achieved by using a `mounted` ref.