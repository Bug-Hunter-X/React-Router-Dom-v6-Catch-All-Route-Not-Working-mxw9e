# React Router Dom v6 Catch All Route Not Working

This repository demonstrates a common issue encountered when using catch-all routes (*) in React Router Dom v6.  The catch-all route, intended to handle any unmatched paths, doesn't function correctly due to its placement within the route hierarchy.

## Problem

The provided example shows a catch-all route (`/*`) nested directly under `Routes`.  In this scenario, the catch-all route will only match if *no other routes* above it match, even if those other routes are more specific.  This makes it ineffective at catching any unexpected paths.

## Solution

The solution involves ensuring that the catch-all route is the last route defined under `<Routes>`. This guarantees it only matches if all other paths have been exhausted.  This example shows how to correctly implement a catch-all route that effectively handles any unmatched path.