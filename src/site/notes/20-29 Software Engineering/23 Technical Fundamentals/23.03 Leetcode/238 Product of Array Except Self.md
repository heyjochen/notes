---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/238-product-of-array-except-self/","tags":["dsa/array"],"created":"2023-07-24T06:25:12.814-05:00","updated":"2023-10-17T07:54:10.766-05:00"}
---

# 238 Product of Array Except Self
## Problem Statement
Given an integer array `nums`, return _an array_ `answer` _such that_ `answer[i]` _is equal to the product of all the elements of_ `nums` _except_ `nums[i]`.
The product of any prefix or suffix of `nums` is **guaranteed** to fit in a **32-bit** integer.
You must write an algorithm that runs in `O(n)` time and without using the division operation.

**Input:** nums = [1,2,3,4]
**Output:** [24,12,8,6]
## Approach
The key to solve this problem is to find out, how the math works at each position. If we look at nums\[1] we see that we want the product of the numbers to the left and the product of the numbers to the right:
`[1,2,3,4]`
1   *   (3\*4)

To do that we can make use of a postfix and a prefix, which tracks the products, as well as an extra results array which will be updated through two loops:
## Solution
```javascript
const productExceptSelf => (nums) = {
	let prefix = 1;
	let postfix = 1;
	let result = [];
	for (let i = 0; i < nums.length; i++) {
		result[i] = prefix
		prefix *= nums[i]
	}
	  
	for (let i = nums.length - 1; i >= 0; i--){
		result[i] *= postfix
		postfix *= nums[i]
	}
	
	return result
};
```
## References
[LC](https://leetcode.com/problems/product-of-array-except-self/)
## Related
[[DSA MOC\|DSA MOC]]