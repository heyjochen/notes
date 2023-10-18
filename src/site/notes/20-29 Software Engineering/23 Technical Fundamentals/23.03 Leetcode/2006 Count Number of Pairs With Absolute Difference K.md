---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/2006-count-number-of-pairs-with-absolute-difference-k/","tags":["dsa/hash"],"created":"2023-10-18T07:00:13.354-05:00","updated":"2023-10-18T07:33:50.850-05:00"}
---

# 2006 Count Number of Pairs With Absolute Difference K
## Problem Statement
Given an integer array `nums` and an integer `k`, return _the number of pairs_ `(i, j)` _where_ `i < j` _such that_ `|nums[i] - nums[j]| == k`.

The value of `|x|` is defined as:

- `x` if `x >= 0`.
- `-x` if `x < 0`.

**Input:** nums = [3,-3, 2,1,5,4], k = 2
**Output:** 4
## Approach
Loop through input array, for each num in nums we record entries in the hash that are k units apart from the num. So we have to keep track of the count at n - k and n + k. 

For the first num in the example it will create following two entries: {1: 1, 5: 1}. If we have a match we add the count of that match to our count. With this example we don't have a match until we hit n = 1.

## Solution
```javascript
var countKDifference = function(nums, k) {
	const hash = {};
	let count = 0;
	for (let n of nums) {
		if (hash[n]) count += hash[n];
		hash[n - k] ? hash[n - k] += 1: hash[n - k] = 1;
		hash[n + k] ? hash[n + k] += 1: hash[n + k] = 1;
	}
	
	return count;
};
```
## Questions
1. What are we using the hash for ?
	We use it to keep track of the occurrences of numbers that are k units apart from the current number.
## References
[LC](https://leetcode.com/problems/count-number-of-pairs-with-absolute-difference-k/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Hash table\|Hash table]]