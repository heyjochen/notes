---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/226-invert-binary-tree/","tags":["dsa/tree"],"created":"2023-11-22T07:29:59.591-06:00","updated":"2023-11-22T07:42:33.192-06:00"}
---

# 226 Invert Binary Tree

## Problem Statement
Given the `root` of a binary tree, invert the tree, and return _its root_.

**Input:** root = [4,2,7,1,3,6,9]
**Output:** [4,7,2,9,6,3,1]
## Approach
We are using a recursive approach so we have to first define a base case:
When the function gets passed a null pointer (meaning calling the function on a left or right branch of a node that has nothing there); you return the null pointer back.

Before we do our swap, we create a temp variable, swap and assign the temp to the swapped variable.

Then we make our recursive calls and in the end return the root.
## Solution
```javascript
var invertTree = function(root) {
  if (root === null) {
    return null;
  }

  // Swap left and right subtrees
  let temp = root.left;
  root.left = root.right;
  root.right = temp;

  // Recursively invert left and right subtrees
  invertTree(root.left);
  invertTree(root.right);

  return root;
};
```
## Questions
#### What is the Base case?
You are getting a null pointer for either left or right branch, then return null
#### How does inverting work?
Creating a temp variable, swapping, reassigning
## References
[LC](https://leetcode.com/problems/invert-binary-tree/description/)
## Related