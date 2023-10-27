---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/342-power-of-four/","tags":["dsa/recursion"],"created":"2023-10-27T07:43:39.761-05:00","updated":"2023-10-27T07:58:41.081-05:00"}
---

# 342 Power of Four
## Problem Statement
Given an integer `n`, return _`true` if it is a power of four. Otherwise, return `false`_.
An integer `n` is a power of four, if there exists an integer `x` such that `n == 4x`.

**Input:** n = 16
**Output:** true

**Input:** n = 5
**Output:** false

**Input:** n = 1
**Output:** true
## Approach
We can solve this with Recursion where we recursively call the function with `n = n / 4`.
The base case has to be defined as `n === 1`, if that is true we return true. 
To get to the base case we have to understand exponents. If the integer `n` is equal to `1` it can be expressed as `4^0`, which satisfies the definition of a power of four.
## Solution
```javascript
var isPowerOfFour = function(n) {
  if (n === 1)  return true
  if (n < 1) return false
  return isPowerOfFour(n / 4)
};
```
## Questions
## References
[LC](https://leetcode.com/problems/power-of-four/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Recursion\|Recursion]]