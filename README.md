# Unexpected Return Value from Tcl proc

This repository demonstrates a subtle issue with Tcl's `proc` command. The problem arises when using conditional statements (like `if`) within a procedure.  The procedure may not return the expected value if the `return` statement isn't carefully placed.

## The Bug

The `bug.tcl` file contains a procedure `badproc` that attempts to return 1 if the input `a` is equal to 1, and 0 otherwise. Due to the way Tcl handles the return value of `if`, the procedure always returns 0 even when `a` is 1.

## The Solution

The `bugSolution.tcl` file provides a corrected version of the procedure. The issue is solved by explicitly returning the correct value in each branch of the conditional statement.