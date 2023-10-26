---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/22-generate-parentheses/","tags":["dsa/recursion"],"created":"2023-10-26T07:10:39.970-05:00","updated":"2023-10-26T07:41:12.340-05:00"}
---

# 22 Generate Parentheses
## Problem Statement
Given `n` pairs of parentheses, write a function to _generate all combinations of well-formed parentheses_.

**Input:** n = 3
**Output:** ["((()))","(()())","(())()","()(())","()()()"]
## Approach
Recognizing the approach to this problem becomes easier once we draw it out in a Trie-like pattern:
```
       (             // Level 1
     /   \
    (     )          // Level 2
   / \   / \
  (   ) (   )        // Level 3
```
Start with the base case and define what happens when it is met. Then each recursive call has two options:
1. We either add an open parenthese and call the function with updated params
2. or we add a close parenthese 

The recursive function does not need to know how many possible combinations there are. It just does its thing and finds all of them via adding function calls to the call stack and from there backtracking.
## Solution
```javascript
var generateParenthesis = function(n) {
	let result = []

	function genRecur(o, c, str){
		if (str.length === n * 2) {
			result.push(str)
			return
		}
		
		if (o < n) {
			genRecur(o + 1, c, str + '(')
		}
		
		if (c < o) {
			genRecur(o, c + 1, str + ')')
		}
	}
  
	genRecur(1, 0, '(')
	return result
};
```
## Questions
## References
[LC](https://leetcode.com/problems/generate-parentheses/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Recursion\|Recursion]]