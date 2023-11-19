---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/155-min-stack/","created":"2023-11-16T07:02:27.386-06:00","updated":"2023-11-16T07:07:53.010-06:00"}
---

# 155 Min Stack
## Problem Statement
Design a stack that supports push, pop, top, and retrieving the minimum element in constant time.

Implement the `MinStack` class:

- `MinStack()` initializes the stack object.
- `void push(int val)` pushes the element `val` onto the stack.
- `void pop()` removes the element on the top of the stack.
- `int top()` gets the top element of the stack.
- `int getMin()` retrieves the minimum element in the stack.

You must implement a solution with `O(1)` time complexity for each function.

**Input**
["MinStack","push","push","push","getMin","pop","top","getMin"]
[[],[-2],[0],[-3],[],[],[],[\|],[-2],[0],[-3],[],[],[],[]]

**Output**
[null,null,null,null,-3,null,0,-2]
## Approach
We use two stacks, one as the "result" stack and one to keep track of minimum Values.
**Push:** If the minStack is empty and the current value is smaller/equal than the last element on the minStack we push the value onto it.
**Pop:** We pop from the stack and if that value equals the last value on the minStack we also pop from the minStack.

The other operations are straightforward
## Solution
```javascript
var MinStack = function() {
  this.stack = []
  this.minStack = []
};

MinStack.prototype.push = function(val) {
  this.stack.push(val)
  if (!this.minStack.length || val <= this.minStack[this.minStack.length - 1]) {
    this.minStack.push(val)
  }
};

MinStack.prototype.pop = function() {
  let x = this.stack.pop()
  if (x === this.minStack[this.minStack.length - 1]) {
    this.minStack.pop()
  }
};

MinStack.prototype.top = function() {
  return this.stack[this.stack.length - 1]
};

MinStack.prototype.getMin = function() {
  return this.minStack[this.minStack.length - 1]
};
```
## Questions
## References
[LC](https://leetcode.com/problems/min-stack/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Stack\|Stack]]