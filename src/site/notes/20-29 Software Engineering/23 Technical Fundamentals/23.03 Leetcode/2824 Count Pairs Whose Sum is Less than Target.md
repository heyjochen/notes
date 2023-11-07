---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/2824-count-pairs-whose-sum-is-less-than-target/","tags":["dsa/hash"],"created":"2023-11-07T07:39:45.985-06:00","updated":"2023-11-07T07:49:47.340-06:00"}
---

# 2824 Count Pairs Whose Sum is Less than Target
## Problem Statement
Given a **0-indexed** integer array `nums` of length `n` and an integer `target`, return _the number of pairs_ `(i, j)` _where_ `0 <= i < j < n` _and_ `nums[i] + nums[j] < target`.

**Input:** nums = [-1,1,2,3,1], target = 2
**Output:** 3
## Approach
If we are sorting the input array we can get our Time complexity from O(N2) to O(log n). From there the solution is similar to Target Sum.
**If the sum of the elements at left and right is less than the target value, it means all pairs with the current left element will also satisfy the condition. So, increment the count by right - left and shift the left pointer to the right.**
## Solution
```javascript
var countPairs = function(nums, target) {
	nums.sort((a,b) => a - b)
	let l = 0,
	r = nums.length - 1,
	count = 0

	while (l < r) {
		if (nums[l] + nums[r] < target) {
			count += (r - l)
			l++
		} else {
			r--
		}
	}

	return count
};
```
## Questions
## References
[LC](https://leetcode.com/problems/count-pairs-whose-sum-is-less-than-target/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Two Pointers\|Two Pointers]]