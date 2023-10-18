---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/217-contains-duplicate/","tags":["dsa/hash"],"created":"2023-07-18T07:20:56.533-05:00","updated":"2023-10-17T07:54:02.613-05:00"}
---

#code/question #code/javascript #code/dsa
# 217 Contains duplicate

## Problem Statement
Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

**Input:** nums = [1,2,3,1]
**Output:** true
## Approach
Either solving by BF, looping through the whole array, by using a hashset or by comparing a Set's size to the array length.
## Solution
```javascript
const containsDuplicate = nums => {
	let hash = {}

	for (let num of nums){
		if (hash[num]) {
			return false
		} else {
			hash[num] = 1
		}
	}
	return true
}
```

```javascript
    return new Set(nums).size !== nums.length
```
## Gotcha

## References
[LC](https://leetcode.com/problems/contains-duplicate/description/)
## Related
[[DSA MOC\|DSA MOC]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Map in JavaScript\|Map in JavaScript]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Set in JavaScript\|Set in JavaScript]]