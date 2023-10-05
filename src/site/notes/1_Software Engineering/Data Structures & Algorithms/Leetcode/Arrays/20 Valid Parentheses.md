---
{"dg-publish":true,"permalink":"/1-software-engineering/data-structures-and-algorithms/leetcode/arrays/20-valid-parentheses/","created":"2023-08-01T07:08:02.270-05:00","updated":"2023-10-05T07:41:04.498-05:00"}
---

#code/question #code/javascript #code/dsa/stack
# 20 Valid Parentheses
## Problem Statement
Given a string `s` containing just the characters `'('`, `')'`, `'{'`, `'}'`, `'['` and `']'`, determine if the input string is valid.

An input string is valid if:
1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.

**Input:** s = "()[]{}"
**Output:** true
## Approach
We init a hashmap for our pairs. Next we handle the base conditions to return early. We then init a stack that keeps track of opening parentheses. If it is not an opened one we pop the top of the stack and evaluate the current closing parentheses, return false if no match.
In the end the stack should be empty.
## Solution
```javascript
const pairs = {
"(": ")",
"[": "]",
"{": "}"
}

var isValid = function(s) {
	if (s.length % 2 === 1) return false
	if (s[0] === "]" || s[0] === ")" || s[0] === "}") return false
	if (s[s.length - 1] === "[" || s[s.length - 1] === "(" || s[s.length - 1] === "{") return false
	
	let stack = []

for (let i=0; i<s.length; i++) {
	// if it's an opening bracket, push into stack
	// else, assume it's closing bracket and check if it matches anything
	if(s[i] === "[" || s[i] === "(" || s[i] === "{") {
		stack.push(s[i])
	} else if (pairs[stack.pop()] !== s[i]) {
		return false
	}
}

return stack.length === 0
};
```
## Questions
1. How do we know that we need a stack?
	Stack is great for nested structures or matching pairs as it keeps track of the opening brackets encountered so far.
2. How do we check for an opening bracket when we encounter a closing bracket?
	Use the hashmap created
## References
[LC](https://leetcode.com/problems/valid-parentheses/)
## Related
[[1_Software Engineering/MOCs/DSA MOC\|DSA MOC]]