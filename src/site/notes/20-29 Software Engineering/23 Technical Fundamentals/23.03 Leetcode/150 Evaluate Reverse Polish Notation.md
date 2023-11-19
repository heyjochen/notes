---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/150-evaluate-reverse-polish-notation/","created":"2023-11-15T07:14:33.281-06:00","updated":"2023-11-15T07:18:50.744-06:00"}
---

# 150 Evaluate Reverse Polish Notation
## Problem Statement
You are given an array of strings `tokens` that represents an arithmetic expression in a [Reverse Polish Notation](http://en.wikipedia.org/wiki/Reverse_Polish_notation).
Evaluate the expression. Return _an integer that represents the value of the expression_.
**Note** that:

- The valid operators are `'+'`, `'-'`, `'*'`, and `'/'`.
- Each operand may be an integer or another expression.
- The division between two integers always **truncates toward zero**.
- There will not be any division by zero.
- The input represents a valid arithmetic expression in a reverse polish notation.
- The answer and all the intermediate calculations can be represented in a **32-bit** integer.

**Input:** tokens = ["2","1","+","3","*"]
**Output:** 9
**Explanation:** ((2 + 1) * 3) = 9

## Approach
The following points are very important:
- The division between two integers always **truncates toward zero**.
- There will not be any division by zero.
This means that 3 / 2 is 1 and not 1.5.
From there we use a stack to come to a solution.
## Solution
```javascript
var evalRPN = function(tokens) {
  let stack = []

  for (const t of tokens) {
    const isOperator = t === '+' || t === '-' || t === '*' || t === '/'
    if (isOperator) {
      const v2 = stack.pop()
      const v1 = stack.pop()
      let v3
      switch (t) {
        case "+": v3 = v1 + v2; break;
        case "-": v3 = v1 - v2; break;
        case "*": v3 = v1 * v2; break;
        case "/":
          if (v2 === 0) {
            throw new Error("Division by zero");
          }
          v3 = Math.trunc(v1 / v2);
          break;
      }
      stack.push(v3)
      continue
    } else {
      stack.push(+t)
    }
  }

  return stack.pop()
};
```
## Questions
## References
[LC](https://leetcode.com/problems/evaluate-reverse-polish-notation/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Stack\|Stack]]