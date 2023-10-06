---
{"dg-publish":true,"permalink":"/1-software-engineering/data-structures-and-algorithms/leetcode/strings/3-longest-substring/","tags":["code/dsa"],"created":"2023-10-06T07:25:54.110-05:00","updated":"2023-10-06T07:47:25.926-05:00"}
---

# 3 Longest Substring
## Problem Statement
Given a string `s`, find the length of the **longest substring** without repeating characters.
**Input:** s = "abcabcbb"
**Output:** 3
## Approach
Sliding Window approach with a Set and two Pointers. We loop through the string via the right pointer and add the character at right to the Set and then get the length. Our while loop removes characters from the left until there are no more duplicates.
## Solution
```javascript
var lengthOfLongestSubstring = function(s) {
	let set = new Set();
	let length = 0;
	let left = 0;
	for (let right = 0; right < s.length; right++) {
		while (set.has(s[right])) {
			set.delete(s[left]);
			left++;
		}
		
		set.add(s[right]);
		length = Math.max(length, right - left + 1);
	}
	return length
};
```
## Questions
## References
[]()
## Related