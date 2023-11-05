---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/88-merge-sorted-array/","tags":["dsa/hash"],"created":"2023-11-02T07:43:58.478-05:00","updated":"2023-11-03T06:26:25.855-05:00"}
---

# 88 Merge Sorted Array
## Problem Statement
You are given two integer arrays `nums1` and `nums2`, sorted in **non-decreasing order**, and two integers `m` and `n`, representing the number of elements in `nums1` and `nums2` respectively.

**Merge** `nums1` and `nums2` into a single array sorted in **non-decreasing order**.

The final sorted array should not be returned by the function, but instead be _stored inside the array_ `nums1`. To accommodate this, `nums1` has a length of `m + n`, where the first `m` elements denote the elements that should be merged, and the last `n` elements are set to `0` and should be ignored. `nums2` has a length of `n`.

**Input:** nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
**Output:** [1,2,2,3,5,6]
## Approach
Three Pointers and assigning values into nums from end. P1 looks at the last entry before the 0 values, P2 at the last entry in nums2 and P3 looks at (m+ n - 1). From there it is a while loop through the array that assigns whatever value at position of the pointers is greater to nums1[p3]. All pointers will be shifted accordingly.
Finally we need another while loop that handles remaining items in nums2.
## Solution
```javascript
var twoSum = function(nums, target) {
    let p1 = m - 1; // Pointer for nums1 (excluding trailing zeros)
    let p2 = n - 1; // Pointer for nums2
    let p3 = m + n - 1; // Pointer for the merged result

    while (p1 >= 0 && p2 >= 0) {
        if (nums1[p1] > nums2[p2]) {
            nums1[p3] = nums1[p1];
            p1--;
        } else {
            nums1[p3] = nums2[p2];
            p2--;
        }
        p3--;
    }

    // If there are remaining elements in nums2, copy them to nums1
    while (p2 >= 0) {
        nums1[p3] = nums2[p2];
        p2--;
        p3--;
    }
};
```
## Questions
## References
[LC](https://leetcode.com/problems/merge-sorted-array/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Two Pointers\|Two Pointers]]