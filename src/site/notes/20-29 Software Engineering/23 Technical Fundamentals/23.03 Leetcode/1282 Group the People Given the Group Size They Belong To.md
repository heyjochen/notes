---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/1282-group-the-people-given-the-group-size-they-belong-to/","tags":["dsa/hash"],"created":"2023-10-20T07:51:09.388-05:00","updated":"2023-10-20T07:55:53.357-05:00"}
---

# 1282 Group the People Given the Group Size They Belong To
## Problem Statement
There are `n` people that are split into some unknown number of groups. Each person is labeled with a **unique ID** from `0` to `n - 1`.

You are given an integer array `groupSizes`, where `groupSizes[i]` is the size of the group that person `i` is in. For example, if `groupSizes[1] = 3`, then person `1` must be in a group of size `3`.

Return _a list of groups such that each person `i` is in a group of size `groupSizes[i]`_.

Each person should appear in **exactly one group**, and every person must be in a group. If there are multiple answers, **return any of them**. It is **guaranteed** that there will be **at least one** valid solution for the given input.
**Input:** groupSizes = [3,3,3,3,3,1,3]
**Output:** [\[5],[0,1,2],[3,4,6]]
## Approach
We are using a Hash Table to store group sizes as a key with a bucket (array) of each persons index as a value. Once one of these buckets has the length that matches the person we push that into the results array and clear out the bucket
## Solution
```javascript
var groupThePeople = function(groupSizes) {
	let result = [],
	hash = {}

	for (const [index, person] of groupSizes.entries()){
		hash[person] ? hash[person].push(index) : hash[person] = [index]
		if (hash[person].length === person) {
			result.push(hash[person]);
			hash[person] = [];
		}
	}
	return result
};
```
## Questions
## References
[LC](https://leetcode.com/problems/group-the-people-given-the-group-size-they-belong-to/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Hash table\|Hash table]]