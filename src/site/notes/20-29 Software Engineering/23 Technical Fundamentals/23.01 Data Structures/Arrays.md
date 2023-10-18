---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-01-data-structures/arrays/","tags":["code/dsa"],"created":"2023-08-07T06:22:06.302-05:00","updated":"2023-10-11T07:03:49.189-05:00"}
---

# Arrays
Arrays are like buckets that hold values.
## Intro
Store value of different type (in JS) at contiguous memory location. Strings are arrays as well.
### Advantages
- Fast access if you have index
### Disadvantages
- Adding or removal from the middle is slow, opposed to Linked List.
## Terms
- Subarray, [1,4,5,2] -> [4,5,2] is a subarray
- Subsequence, [1,4,5,2] -> [1,4,2] is a subsequence

The difference is that a subarray can't have any element in between, it has to be contiguous. A subsequence can be derived from the original array by deleting elements, but the order has to stay the same
## Time Complexity
- Access: O(1)
- Search: O(n)
- Search sorted: O(log n)
- Insert: O(n)
- Insert at the end (.push()): O(1)
- Remove: O(n)
- Remove at the end (.pop()): O(1)
## Look out for in interview
- Are there duplicates in the array? Would this affect the answer? 
- Remember the bounds when using indexes
- .slice() and .concat() need O(n) time, prefer subarray
## Corner Cases
- Empty sequence
- Duplicates
- Sequence with repeated elements
- Sequence with 1 or 2 elements
## Techniques
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Sliding Window\|Sliding Window]] - Subarray / Substring
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Two Pointers\|Two Pointers]]
## Essential Questions

{ .block-language-dataview}
## References
## Related
