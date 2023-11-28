---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/876-middle-of-the-linked-list/","tags":["dsa/linked_list"],"created":"2023-11-28T07:50:19.687-06:00","updated":"2023-11-28T08:06:42.296-06:00"}
---

# 876 Middle of the Linked List
## Problem Statement
Given the `head` of a singly linked list, return _the middle node of the linked list_.

If there are two middle nodes, return **the second middle** node.
**Input:** head = [1,2,3,4,5]
**Output:** [3,4,5]
## Approach
This can be solved with a fast and slow pointer approach. Once the fast pointer reaches the end of the linked list our slow pointer will be in the middle of the linked list.
Our while loop has to check for `fast && fast.next` as fast could possibly be undefined in the assignment.
## Solution
```javascript
var middleNode = function(head) {
  let fast = head
  let slow = head

  while (fast && fast.next) {
    slow = slow.next
    fast = fast.next.next
  }
  return slow
};
```
## Questions
## References
[LC](https://leetcode.com/problems/middle-of-the-linked-list/description/)
## Related