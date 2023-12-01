---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/234-palindrome-linked-list/","tags":["dsa/linked_list"],"created":"2023-12-01T06:47:01.605-06:00","updated":"2023-12-01T07:00:53.951-06:00"}
---

# 234 Palindrome Linked List
## Problem Statement
Given the `head` of a singly linked list, return `true` _if it is a_ _palindrome_ _or_ `false` _otherwise_.

**Input:** head = [1,2,2,1]
**Output:** true
## Approach
- BigO(N) space: Additional Linked List which will be reversed
- BigO(1) space: Finding middle node, reversing second half, comparing second half to first
## Solution
```javascript
function reverseList(node) {
  let current = node;
  let next = null;
  let prev = null;

  while (current) {
    next = current.next;
    current.next = prev;
    prev = current;
    current = next;
  }

  return prev;
}

function findMiddle(head) {
  let slow = head;
  let fast = head;

  while (fast && fast.next) {
    slow = slow.next;
    fast = fast.next.next;
  }

  return slow;
}

var isPalindrome = function(head) {
  let middle = findMiddle(head);

  let reversedSecondHalf = reverseList(middle);

  let firstHalf = head;
  let secondHalf = reversedSecondHalf;

  while (secondHalf) {
    if (firstHalf.val !== secondHalf.val) {
      return false;
    }
    firstHalf = firstHalf.next;
    secondHalf = secondHalf.next;
  }

  return true;
};
```
## Questions
## References
[LC](https://leetcode.com/problems/palindrome-linked-list/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Linked List\|Linked List]]