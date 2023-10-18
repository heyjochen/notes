---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/3-longest-substring/","tags":["dsa/string"],"created":"2023-10-06T07:25:54.110-05:00","updated":"2023-10-17T07:56:24.353-05:00"}
---

# 3 Longest Substring
## Problem Statement
Given a string `s`, find the length of the **longest substring** without repeating characters.
**Input:** s = "abcabcbb"
**Output:** 3
## Approach
Sliding Window approach with a Set and two Pointers. We loop through the string via the right pointer and add the character at right to the Set and then get the length. Once there is a duplicate our while loop kicks in and removes characters from the left and shifts the left pointer. Once the set is clear we start looking for a longest substring again.
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
[LC](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Strings\|Strings]]
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Two Pointers\|Two Pointers]]