---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/232-implement-queue-using-stacks/","tags":["dsa/hash"],"created":"2023-11-14T07:39:52.809-06:00","updated":"2023-11-14T07:57:28.336-06:00"}
---

# 232 Implement Queue using Stacks
## Problem Statement
Implement a first in first out (FIFO) queue using only two stacks. The implemented queue should support all the functions of a normal queue (`push`, `peek`, `pop`, and `empty`).

Implement the `MyQueue` class:

- `void push(int x)` Pushes element x to the back of the queue.
- `int pop()` Removes the element from the front of the queue and returns it.
- `int peek()` Returns the element at the front of the queue.
- `boolean empty()` Returns `true` if the queue is empty, `false` otherwise.
## Approach
We know that a Queue is a FIFO data structure while a stack is a LIFO data structure. 
When you **push (enqueue)** an element into the queue, the element is simply added to stack1.
But when it comes to **dequeue with the pop() and peek()** operations we make sure that the oldest element is at the top of the stack and there need to transfer them before performing the operation. If the stack2 is not empty it means that they are already in the correct order and we can perform the operation.

How do you reverse the order? 
```javascript
 if (this.stack2.length === 0) {
    // Transfer elements from stack1 to stack2 to reverse the order
    while (this.stack1.length > 0) {
      this.stack2.push(this.stack1.pop());
    }
  }
```
For Pop the Operation looks like so:
```javascript
  return this.stack2.pop();
```
For Peek the Operation looks like so:
```javascript
  return this.stack2[this.stack2.length - 1];
```
## Solution
```javascript
/**
 * Initialize your data structure here.
 */
var MyQueue = function() {
  this.stack1 = [];
  this.stack2 = [];
};

/**
 * Push element x to the back of queue.
 * @param {number} x
 * @return {void}
 */
MyQueue.prototype.push = function(x) {
  this.stack1.push(x);
};

/**
 * Removes the element from in front of queue and returns that element.
 * @return {number}
 */
MyQueue.prototype.pop = function() {
  if (this.stack2.length === 0) {
    while (this.stack1.length > 0) {
      this.stack2.push(this.stack1.pop());
    }
  }
  return this.stack2.pop();
};

/**
 * Get the front element.
 * @return {number}
 */
MyQueue.prototype.peek = function() {
  if (this.stack2.length === 0) {
    while (this.stack1.length > 0) {
      this.stack2.push(this.stack1.pop());
    }
  }
  return this.stack2[this.stack2.length - 1];
};

/**
 * Returns whether the queue is empty.
 * @return {boolean}
 */
MyQueue.prototype.empty = function() {
  return this.stack1.length === 0 && this.stack2.length === 0;
};

// Example usage:
const myQueue = new MyQueue();
myQueue.push(1);
myQueue.push(2);
console.log(myQueue.peek()); // Output: 1
console.log(myQueue.pop());  // Output: 1
console.log(myQueue.empty()); // Output: false

```
## Questions
## References
[LC](https://leetcode.com/problems/implement-queue-using-stacks/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Stack\|Stack]]