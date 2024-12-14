# React Router v6 Catch-all Route Conflict

This repository demonstrates a common issue in React Router v6 related to catch-all routes (`/*`). When a catch-all route is defined, it can unexpectedly match routes that should be handled by other, more specific routes, leading to incorrect page rendering or other unexpected behavior.

## Problem

The problem arises when a catch-all route is placed after more specific routes. The catch-all route will always match, even if a more specific route exists. This can lead to the catch-all route being rendered instead of the intended route.

## Solution

The solution is to place the catch-all route at the very end of the `Routes` component. This ensures that it only matches when no other route matches the URL.