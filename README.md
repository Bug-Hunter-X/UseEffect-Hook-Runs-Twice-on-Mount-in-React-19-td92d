# React 19 useEffect Hook Runs Twice on Mount

This repository demonstrates a seemingly innocuous issue where the `useEffect` hook in React 19 runs twice on component mount, despite having an empty dependency array.  This unexpected behavior can lead to performance issues and incorrect state management.  The repository includes both the problematic code and a solution.

## Problem

The `useEffect` hook, even with `[]` as its dependency array, executes twice. This contradicts the expected single execution on mount.

## Solution

The solution involves ensuring that no side effects trigger re-renders within the `useEffect` hook that could lead to unexpected secondary execution.