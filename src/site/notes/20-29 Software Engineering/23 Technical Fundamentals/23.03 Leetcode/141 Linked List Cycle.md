---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/141-linked-list-cycle/","tags":["dsa/linked_list"],"created":"2023-11-30T06:53:52.841-06:00","updated":"2023-11-30T07:38:02.003-06:00"}
---

# 141 Linked List Cycle
## Problem Statement
Given `head`, the head of a linked list, determine if the linked list has a cycle in it.

There is a cycle in a linked list if there is some node in the list that can be reached again by continuously following the `next` pointer. Internally, `pos` is used to denote the index of the node that tail's `next` pointer is connected to. **Note that `pos` is not passed as a parameter**.

Return `true` _if there is a cycle in the linked list_. Otherwise, return `false`.

**Input:** head = [3,2,0,-4], pos = 1
**Output:** true
## Approach
There is two possible approaches:
- Using two pointers and a Set. BigO(N).
- Slow and Fast Pointers. BigO(1)
## Solution
```javascript
// First solution
function hasCycle(head) {
  let set = new Set()
  let current = head
  while (current) {
    if (set.has(current.val)) {
      return true
    }

    set.add(current.val)
    current = current.next
  }

  return false
}

// Second Solution
var hasCycle = function(head) {
	let slow = head
	let fast = head

	while (fast && fast.next) {
		fast = fast.next.next
		slow = slow.next
		if (fast === slow) {
			return true
		}
	}

	return false
};
```
## Questions
## References
[LC](https://leetcode.com/problems/reverse-linked-list/description/)
## Related