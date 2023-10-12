---
{"dg-publish":true,"permalink":"/software-engineering/data-structures-and-algorithms/leetcode/arrays/217-contains-duplicate/","tags":["code/dsa/technique"],"created":"2023-07-18T07:20:56.533-05:00","updated":"2023-10-05T07:42:21.826-05:00"}
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
[[Software Engineering/MOCs/DSA MOC\|DSA MOC]]
[[Software Engineering/Languages/Javascript/Map in JavaScript\|Map in JavaScript]]
[[Software Engineering/Languages/Javascript/Set in JavaScript\|Set in JavaScript]]