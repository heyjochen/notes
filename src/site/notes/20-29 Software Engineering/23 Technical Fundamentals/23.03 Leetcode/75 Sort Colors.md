---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/75-sort-colors/","created":"2023-11-09T08:04:27.864-06:00","updated":"2023-11-10T07:51:47.497-06:00"}
---

# 75 Sort Colors
## Problem Statement
Given an array `nums` with `n` objects colored red, white, or blue, sort them **[in-place](https://en.wikipedia.org/wiki/In-place_algorithm)** so that objects of the same color are adjacent, with the colors in the order red, white, and blue.

We will use the integers `0`, `1`, and `2` to represent the color red, white, and blue, respectively.

You must solve this problem without using the library's sort function.

**Input:** nums = [2,0,2,1,1,0]
**Output:** [0,0,1,1,2,2]

## Approach
BF: Would be two loops, first to create counts for each number, then second to overwrite array values.

Optimized: We have three pointers - i, low and high and are partitioning the array in three parts with the number 1 being the pivot point. In case of arr[i] being 2 we need to make sure to not increment i because the new element at index `i` (which was originally at the `high` index) hasn't been checked yet. For the other cases we increment the i index by one.

When I the current number is 0 I want to make sure that it will be moved to the low point, when the number is 2 I want to make sure that it will be moved to the high point.
When the number is 1 I don't care and move on.
## Solution
```javascript
var sortColors = function(arr) {
    let low = 0;
    let high = arr.length - 1;
    let i = 0;

    while (i <= high) {
        switch (arr[i]) {
            case 0:
                [arr[i], arr[low]] = [arr[low], arr[i]];
                low++;
                i++;
                break;
            case 1:
                i++;
                break;
            case 2:
                [arr[i], arr[high]] = [arr[high], arr[i]];
                high--;
                break;
        }
    }

    return arr;
};
```
## Questions
## References
[LC](https://leetcode.com/problems/sort-colors/description/)
## Related