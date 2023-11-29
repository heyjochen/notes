---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/206-reverse-linked-list/","tags":["dsa/linked_list"],"created":"2023-11-29T07:14:16.081-06:00","updated":"2023-11-29T07:18:01.717-06:00"}
---

# 206 Reverse Linked List
## Problem Statement
Given the `head` of a singly linked list, reverse the list, and return _the reversed list_.

**Input:** head = [1,2,3,4,5]
**Output:** [5,4,3,2,1]
## Approach
Three Pointer approach. We first save the next node, then reverse the link, then move previous to current, then move current to next. We return previous as this is the new head of the reversed linked list.
## Solution
```javascript
function reverseLinkedList(head) {
  let current = head;
  let previous = null;
  let next = null;

  while (current !== null) {
    next = current.next;
    current.next = previous;
    previous = current;
    current = next;
  }

  return previous
}
```
## Questions
## References
[LC](https://leetcode.com/problems/reverse-linked-list/description/)
## Related