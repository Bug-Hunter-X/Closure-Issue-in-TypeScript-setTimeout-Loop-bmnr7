# TypeScript Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue encountered when using `setTimeout` within a loop in TypeScript.

## Problem

The `printNumbers2` function aims to print numbers from 1 to n with a slight delay using `setTimeout`. However, due to the nature of closures, by the time the `setTimeout` callbacks execute, the loop has already completed, and 'i' will hold its final value (n+1). 

## Solution

The solution involves using an immediately invoked function expression (IIFE) or `let` within the loop to create a new scope for each iteration, capturing the current value of `i`.