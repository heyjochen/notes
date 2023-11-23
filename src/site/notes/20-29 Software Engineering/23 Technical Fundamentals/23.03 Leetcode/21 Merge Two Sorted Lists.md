---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/21-merge-two-sorted-lists/","tags":["dsa/linked_list"],"created":"2023-11-21T07:29:43.696-06:00","updated":"2023-11-21T07:45:52.444-06:00"}
---

# 21 Merge Two Sorted Lists
## Problem Statement
You are given the heads of two sorted linked lists `list1` and `list2`.

Merge the two lists into one **sorted** list. The list should be made by splicing together the nodes of the first two lists.

Return _the head of the merged linked list_.

**Input:** list1 = [1,2,4], list2 = [1,3,4]
**Output:** [1,1,2,3,4,4]
## Approach
Using a dummy node to simplify the process and have a pointer current towards dummy.
The dummy node itself does not hold any meaningful data from the input lists. Instead, it serves as a starting point and helps avoid special cases for the head of the merged list.
The `current` pointer is then used to iterate and build the merged list. It starts pointing to the dummy node, and as nodes from `list1` and `list2` are merged, the `current.next` property is updated to link to the newly merged node.

Initialize `current1` and `current2` pointers for the two sorted input lists. Use a while loop to iterate while both pointers are not null. Compare the values of the current nodes in the input lists. Append the smaller node to the merged list and move the corresponding pointer to the next node.

The merged list starts from the next node of the dummy node. Return the head of the merged linked list.
## Solution
```javascript
var mergeTwoLists = function(list1, list2) {
  const dummy = new ListNode();
  let current = dummy;

  let current1 = list1;
  let current2 = list2;

  while (current1 !== null && current2 !== null) {
    if (current1.val <= current2.val) {
      current.next = current1;
      current1 = current1.next;
    } else {
      current.next = current2;
      current2 = current2.next;
    }

    current = current.next;
  }

  if (current1 !== null) {
    current.next = current1;
  }

  if (current2 !== null) {
    current.next = current2;
  }

  return dummy.next;
};
```
## Questions
## References
[LC](https://leetcode.com/problems/merge-two-sorted-lists/description/)
## Related