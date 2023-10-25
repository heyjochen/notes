---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/344-reverse-string/","tags":["dsa/recursion"],"created":"2023-10-25T07:22:51.877-05:00","updated":"2023-10-25T07:30:07.515-05:00"}
---

# 344 Reverse String
## Problem Statement
Write a function that reverses a string. The input string is given as an array of characters `s`. You must do this by modifying the input array [in-place](https://en.wikipedia.org/wiki/In-place_algorithm) with `O(1)` extra memory.
**Input:** s = ["h","e","l","l","o"]
**Output:** ["o","l","l","e","h"]
## Approach
The BF approach would be to use a Left and Right Pointer to loop through the array while L < R. At each iteration we would swap the chars and increase/decrease the pointers.
The solution we are interested in is of recursive nature though:

We create a helper function, that takes in the left and right pointer, checks the base case of `if (l < r)` and then does the swap and calls itself with the updated pointers.
## Solution
```javascript
var reverseString = function(s) {
	function recursiveSwap(l,r){
		if (l < r) {
			[s[l], s[r]] = [s[r], s[l]]
			recursiveSwap(l + 1, r - 1)
			}
	}
	recursiveSwap(0, s.length - 1)
};
```
## Questions
## References
[LC](https://leetcode.com/problems/reverse-string/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Recursion\|Recursion]]