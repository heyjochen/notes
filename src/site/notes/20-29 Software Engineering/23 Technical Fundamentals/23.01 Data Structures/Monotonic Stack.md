---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-01-data-structures/monotonic-stack/","tags":["code/dsa/stack","code/dsa/technique"],"created":"2023-10-03T07:57:31.716-05:00","updated":"2023-10-12T07:53:43.406-05:00"}
---

# Monotonic Stack
## Problems used for
- Next greater/smaller element
- Previous greater/smaller element

We always go through an array from left to right
## What is a monotonic stack?
1. Strictly increasing - Every element is strictly greater than the previous - `[1, 4, 5, 8, 9]`
2. Non-decreasing - Every element is greater or equal than the previous - `[1, 4, 5, 5, 8, 9, 9]`
3. Strictly decreasing - Every element is strictly smaller than the previous - `[9, 8, 5, 4, 1]`
4. Non-increasing - Every element is smaller or equal than the previous - `[9, 9, 8, 5, 5, 4, 1]`

The right most element is at the top, the left most at the bottom of the stack.
## How does the function we build work?
- Use a stack and **traverse** the array
- Initialize an results array with length of incoming array filled with 0 / -1
- The stack tracks the index' of elements related to a condition
- We pop() from the top of the stack **WHILE** we have something on the stack and that element at the top of the stack is smaller (depending on condition) than the element at index i
- Then we use the element at the top of the stack, overwrite the value in the results array at that index with the current index of our for loop
- After the while loop we add an element to the stack

## What is the relationship between problem statement and stack?
The relation is inverse:
1. Greater -> Decreasing stack
2. Smaller -> Increasing stack

## How can we find out which stack we have to use?
Finding the next greater element means that the element at the top of the stack has to be smaller than the current element

## Questions
## Terms
## References
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.03 Leetcode/739 Daily Temperatures\|739 Daily Temperatures]]