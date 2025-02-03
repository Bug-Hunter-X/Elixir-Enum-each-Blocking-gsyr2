# Elixir Enum.each Blocking Issue

This repository demonstrates a common issue encountered when using `Enum.each` in Elixir with a function that performs a long-running operation.

The problem is that `Enum.each` blocks the main process while performing the iterative task.  If an operation inside the loop takes a considerable amount of time, the entire program will appear frozen or unresponsive.

This example shows how to address this issue by using `Task.async` to run the operation concurrently, preventing blocking.