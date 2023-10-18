---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/167-two-sum-ii/","tags":["dsa/array","code/dsa/two_pointers"],"created":"2023-07-24T07:01:19.034-05:00","updated":"2023-10-17T07:53:38.913-05:00"}
---

# 167 Two Sum II
## Problem Statement
Given a **1-indexed** array of integers `numbers` that is already **_sorted in non-decreasing order_**, find two numbers such that they add up to a specific `target` number. Let these two numbers be `numbers[index1]` and `numbers[index2]` where `1 <= index1 < index2 < numbers.length`.

Return _the indices of the two numbers,_ `index1` _and_ `index2`_, **added by one** as an integer array_ `[index1, index2]` _of length 2._

The tests are generated such that there is **exactly one solution**. You **may not** use the same element twice.

Your solution must use only constant extra space.

**Input:** numbers = [2,7,11,15], target = 9
**Output:** [1,2]
## Approach
Using Two Pointers to traverse while they haven't met. Build sum and check against being equal, greater or smaller, then decide if to return or shift the pointers.
## Solution
```javascript
var twoSum = function (numbers, target) {
  let [left, right] = [0, numbers.length - 1];

  while (left < right) {
    const sum = numbers[left] + numbers[right];

    const isTargetSum = sum === target;
    const isGreater = sum > target;
    const isLesser = sum < target;

    if (isTargetSum) {
      return [left + 1, right + 1];
    }

    if (isGreater) {
      right--;
    }

    if (isLesser) {
      left++;
    }
  }
  return [-1, -1];
};
```
## Questions
- How can we use the sorted input array to our advantage?
- What checks do I need to do and what happens then? 
	Compare sum against target
- How do you know which pointer to shift? 
	If sum is smaller increase left, if sum is greater decrease right
- What kind of loop do we need to use?
	While loop until the pointers meet
## References
[LC](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/description/)
## Related
[[DSA MOC\|DSA MOC]]
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Two Pointers\|Two Pointers]]