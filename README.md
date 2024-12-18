# React useState Hook Unexpected Behavior

This repository demonstrates a subtle bug related to React's `useState` hook and how multiple state updates within a single event handler might not always behave as expected.  The issue stems from React's batching of state updates for performance optimization. While generally beneficial, this can lead to unexpected results if not properly understood.

## Problem
The provided code updates the count state twice within a single click event. However, due to React's batching, only the final update is reflected in the UI. This might lead to unexpected behavior in situations where the update function depends on the previous state.