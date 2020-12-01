# Data Structures

## What are Collections?

- Plain English: A grouping of similar items like certain kinds of objects
- Ex: Arrays and Objects (aka associative arrays that use key-value pairs)

## What is a Set?

- unordered collection, unique values

## What is a Map?

- unordered collection, not unique values
- key-value pairs of which we can immediately find data by looking up key

## What is a List?

- ordered, non-unique collection

## What Data Structure is similar to Recursion?

- Stack data structure - LIFO (last in first out)
- Recursion's last recursive call is the first thing returned

## What is an Interative vs Recursive Function?

## Algorithms

- When creating pseudocode for algos remember to think of Big O Notation and how your algo could be refactored for efficiency (depending on dataset increase)
- Learn at least 3 algo, solidly
  1. Sorting algo
  2. Searching algo
  3. Bonus algo of your choosing

## Bubble Sort

- Naive sorting algo that we don't actually want to use
- Walk through the array and compare each number
- Swap number to sort from lowest to highest
- Will not be sorted on first pass so will need to go through array multiple times until sorted
- O(1) space
- O(n^2) time

## Quick Sort

- Get the 'pivot' or middle number of the array
- Then sort all the numbers in the array so all numbers less are to the left of the pivot and all numbers more than the pivot are to the right
- Then find a new pivot in the left half and right half and repeat

## Merge Sort

- Divide and conquer technique
- Best done recursively
- O(n log n) time
  - log n for each split
  - n for each comparison operation
- O(n) space
  - temp copy of array must be made to hold sorted list as they are moved over from unsorted list
- Splits halves recursively until we have single elements

## Binary Search

- O(log n) time
- Phonebook example
- Must already be sorted
- Find the midpoint and compare to target value
- Depending on if the midpoint is lower or higher than target then we know to search in the left or right half of the array
- Reset starting or ending index of part of the array that you will continue your search in
