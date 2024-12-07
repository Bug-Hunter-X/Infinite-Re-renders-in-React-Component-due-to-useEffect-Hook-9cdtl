# Infinite Re-renders in React Component

This repository demonstrates a common issue in React applications where an infinite rendering loop occurs due to an improperly used `useEffect` hook.  The `useEffect` hook, when used without specifying dependencies, will cause the component to re-render endlessly.

## Bug Description

The provided `MyComponent` suffers from an infinite re-render loop. Every time the component renders, the `useEffect` hook runs, causing a re-render. This happens because the `useEffect` hook does not include `count` in its dependency array, leading to a continuous cycle.

## Solution

The solution involves correctly specifying the dependencies array within the `useEffect` hook. By including `count` in the array, the hook only executes when the value of `count` changes. 
