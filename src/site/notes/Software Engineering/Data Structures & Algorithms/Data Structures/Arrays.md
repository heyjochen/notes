---
{"dg-publish":true,"permalink":"/software-engineering/data-structures-and-algorithms/data-structures/arrays/","tags":["code/dsa"],"created":"2023-08-07T06:22:06.302-05:00","updated":"2023-10-11T07:03:49.189-05:00"}
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
[[Software Engineering/Data Structures & Algorithms/Algorithms & Techniques/Sliding Window\|Sliding Window]] - Subarray / Substring
[[Software Engineering/Data Structures & Algorithms/Algorithms & Techniques/Two Pointers\|Two Pointers]]
## Essential Questions
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/15 Three Sum\|15 Three Sum]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/167 Two Sum II\|167 Two Sum II]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/217 Contains duplicate\|217 Contains duplicate]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/347 Top K Frequent Elements\|347 Top K Frequent Elements]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/238 Product of Array Except Self\|238 Product of Array Except Self]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/49 Group Anagrams\|49 Group Anagrams]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/739 Daily Temperatures\|739 Daily Temperatures]]
- [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/20 Valid Parentheses\|20 Valid Parentheses]]

{ .block-language-dataview}
## References
## Related
