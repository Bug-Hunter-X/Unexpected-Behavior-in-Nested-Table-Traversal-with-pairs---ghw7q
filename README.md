# Lua Nested Table Traversal Bug

This repository demonstrates a subtle bug that can occur when traversing nested tables in Lua using the `pairs` iterator.  The issue arises from the fact that `pairs` does not guarantee any specific iteration order, and modifying the table during iteration can lead to unexpected results.

## Bug Description
The `bug.lua` file contains a function `foo` that recursively traverses a nested table. However, because the order of iteration is not guaranteed, if the table structure is changed during the traversal, the results may not be what is expected.

## Solution
The `bugSolution.lua` file provides a solution by using a different approach that avoids the potential issues related to `pairs` iteration order. The solution provides a more predictable traversal of the table.

## How to Reproduce
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `lua bug.lua`. This will show the unexpected result.
4. Run `lua bugSolution.lua`. This will demonstrate the corrected behavior.