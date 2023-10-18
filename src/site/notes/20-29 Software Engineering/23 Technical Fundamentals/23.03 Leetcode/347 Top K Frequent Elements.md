---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/347-top-k-frequent-elements/","tags":["dsa/array","dsa/hash"],"created":"2023-07-19T06:08:23.561-05:00","updated":"2023-10-17T07:54:31.642-05:00"}
---

# 347 Top K Frequent Elements
## Problem Statement
Given an integer array `nums` and an integer `k`, return _the_ `k` _most frequent elements_. You may return the answer in **any order**.

**Input:** nums = [1,1,1,2,2,3], k = 2
**Output:** [1,2]
## Approach
There are three parts to this approach:
1. We set up a map to add counts of each entry in the input array. [[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Map to count occurrences in array\|Map to count occurrences in array]]
2. We loop over the map and add entries to our bucket at position of the count that equals the number [[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Set to keep track of values\|Set to keep track of values]]
3. We then add those into our results array, if length is equal k we break and return result
## Solution
```javascript
var topKFrequent = function(nums, k) {
	const freqMap = new Map();
	const bucket = [];
	const result = [];
	
	for (let num of nums) {
		freqMap.set(num, (freqMap.get(num) || 0) + 1);
	}
	
	for (let [num, freq] of freqMap) {
		bucket[freq] = (bucket[freq] || new Set()).add(num);
	}
	
	for (let i = bucket.length-1; i >= 0; i--) {
		if(bucket[i]) result.push(...bucket[i]);
		if(result.length === k) break;
	}
	
	return result;
};

topKFrequent([1,1,1,2,2,2,3,3,4,4,4],3)
```
## Gotcha
- Using a Map makes it easy and concise to keep track of the counts. 
- Using a Set is not there to ensure uniqueness, that is more or less handled by the Map, it is there to have an easy way to keep track
- The second loop will create a Set at bucket\[freq]
- The first if-statement in the last for-loop is there to not break our loop as there could be undefined entries in our bucket in between numbers
## References
[LC](https://leetcode.com/problems/top-k-frequent-elements/)
## Related
[[DSA MOC\|DSA MOC]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Set to keep track of values\|Set to keep track of values]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Map to count occurrences in array\|Map to count occurrences in array]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Map in JavaScript\|Map in JavaScript]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Set in JavaScript\|Set in JavaScript]]