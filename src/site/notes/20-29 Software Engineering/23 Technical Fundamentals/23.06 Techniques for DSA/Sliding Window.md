---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-06-techniques-for-dsa/sliding-window/","tags":["code/javascript","code/dsa/technique"],"created":"2023-08-07T06:55:47.313-05:00","updated":"2023-10-06T07:56:11.783-05:00"}
---

# Sliding Window
Sliding Window is a technique used for common problems that have to do with a subarray or sublist. 
Often we are asked to calculate something among all contiguous subarrays. At the least it comes with *two Pointers* and usually you keep track of the previous best solution.

The Two Pointers usually move in the same direction and never overtake each other.

Giveaway for sliding window:
- something optimal, like **longest** or **shortest** **sequence**

Two important questions:
- When do I grow the window?
	- I would suggest growing initially until we reach a condition, usually when the right pointer is >= K - 1
- When do I shrink it?
	- After every slide to the right

---
> Given an array, find the average of all contiguous subarrays of size ‘K’ in it.
## Input
`Array: [1, 3, 2, 6, -1, 4, 1, 8, 2], K=5`
## Output
`Output: [2.2, 2.8, 2.4, 3.6, 2.8]`
## BF Solution
We would loop through the array and count the sum of every subarray with the length of K and divide the sum by K.
## Time complexity
For every element in the input array N we are calculating the sum of its next K elements, therefore Big O is (N * K). 
## Optimization
We can optimize the Algorithm as whenever we ware calculating the sum of K elements we have overlapping elements that don't need to be recalculated.
Instead we can remove the leftmost element and add the rightmost element, by doing that the Time complexity comes down to O (N).
## Questions
- For the BF Solution: How many iterations do we have in our outer loop? arr.length - 5 + 1
- For the BF Solution: How do we iterate through the inner loop?
- What are the two parts of this technique?
	- Calculating the sum
	- Sliding the window
- In what part of the loop are we calculating the sum and in what part are we sliding the window?
- How do you define the condition where the sliding happens?
- When are we sliding the window?
---
## References
- [1876. Substrings of Size Three with Distinct Characters](https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/)
- [1343. Number of Sub-arrays of Size K and Average Greater than or Equal to Threshold](https://leetcode.com/problems/number-of-sub-arrays-of-size-k-and-average-greater-than-or-equal-to-threshold/)
- [2269. Find the K-Beauty of a Number](https://leetcode.com/problems/find-the-k-beauty-of-a-number/)
## Related
[LC](https://leetcode.com/tag/sliding-window/)