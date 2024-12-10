# React Router v6 Catch-All Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router DOM v6.  The catch-all route, intended to handle any unmatched paths, is unexpectedly not functioning.

The `App.js` file contains the buggy code, while `AppSolution.js` presents a corrected version.

## Problem

The `/*` route should render the `NotFound` component when a user navigates to a path not explicitly defined (e.g., `/nonexistent`). However, in the original implementation, this doesn't happen. Other routes like `/` and `/about` work correctly.

## Solution

The solution involves ensuring that the catch-all route is placed *last* within the `Routes` component.  This ensures it only matches paths that have not already been matched by other more specific routes. 