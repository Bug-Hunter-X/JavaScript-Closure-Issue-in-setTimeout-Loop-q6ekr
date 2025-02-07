# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that often arises when using `setTimeout` within a loop.  The problem involves the incorrect scoping of variables within asynchronous callbacks, leading to unexpected results.

## The Problem

The `bug.js` file contains a function that attempts to log numbers 0-9 to the console with a one-second delay between each number.  Due to the asynchronous nature of `setTimeout` and JavaScript's variable scoping rules, the output is not as expected.

## The Solution

The `bugSolution.js` file provides a corrected version of the function.  It addresses the closure problem by using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that each `setTimeout` callback has its own copy of the loop variable `i`.