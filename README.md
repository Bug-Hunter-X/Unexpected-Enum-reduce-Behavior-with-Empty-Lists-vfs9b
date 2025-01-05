# Elixir Enum.reduce Unexpected Behavior

This repository demonstrates a subtle issue with `Enum.reduce` in Elixir when dealing with empty lists and more complex functions within the reduce operation.  The core problem is that the code implicitly assumes the list will never be empty, and there's no explicit handling for that edge case.

## Bug Description
The initial code uses `Enum.reduce` to sum numbers greater than 3 from a list. If the list is empty, the result is 0 as expected.  However, this behaviour might not be consistent with more complex scenarios.