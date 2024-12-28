# Lua Nested Table Iteration Bug

This repository demonstrates a common error encountered when iterating through nested tables in Lua. The `pairs` iterator can behave unexpectedly if the table is modified during iteration, leading to elements being skipped.

## The Bug

The `bug.lua` file contains a function `foo` that recursively iterates through a nested table.  However, if the table is modified during iteration (even indirectly through recursive calls), `pairs` might not iterate over all elements correctly.

## The Solution

The `bugSolution.lua` file provides a solution using a copy of the table to avoid modification during the iteration process. This ensures that all elements are iterated over reliably.