# React 19 useEffect Bug

This repository demonstrates a common bug in React 19 involving the `useEffect` hook.  The issue arises when the dependency array is incorrectly managed, leading to unintended re-renders.

## Bug Description

The `useEffect` hook is designed to perform side effects based on changes in its dependencies.  However, if the dependency array is omitted or incorrectly specified, the effect may run on every render, causing performance problems or unexpected behavior. 

## Solution

The solution involves correctly specifying the dependency array to include all state variables or props used within the effect.  If the effect needs to run only once on mount, an empty array `[]` should be passed as the dependency array. 

This example demonstrates both the incorrect and corrected versions of the code.