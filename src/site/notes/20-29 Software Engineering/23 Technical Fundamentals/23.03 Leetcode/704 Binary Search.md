---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/704-binary-search/","created":"2023-10-30T06:53:09.665-05:00","updated":"2023-10-30T07:33:15.671-05:00"}
---

# 704 Binary Search
## Problem Statement
Given an array of integers `nums` which is sorted in ascending order, and an integer `target`, write a function to search `target` in `nums`. If `target` exists, then return its index. Otherwise, return `-1`.
You must write an algorithm with `O(log n)` runtime complexity.
**Input:** nums = [-1,0,3,5,9,12], target = 9
**Output:** 4
## Approach
Two Pointers Low and High used as boundaries

## Solution
```javascript
var search = function(arr, val) {
	let low = 0
    let high = nums.length-1
    
    while (low < high) {
        let mid = low + Math.floor((high - low + 1) / 2);
        if (target < nums[mid]) {
            high = mid - 1
        } else {
            low = mid
        } 
    }
    return nums[low] === target ? low : -1
}
```
## Questions
- How are we looping?
	We are using a while loop that runs while low < high. Once that loops stops running we know that they are pointing to the same element.
- How are we building the mid point?
	`low + Math.floor((high - low + 1) / 2)` calculates the index of the mid point relative to the current subarray. Without adding low we would calculate the mid-index of the whole array.
- 
## References
[LC](https://leetcode.com/problems/binary-search/description/)
## Related
[[Searching\|Searching]]