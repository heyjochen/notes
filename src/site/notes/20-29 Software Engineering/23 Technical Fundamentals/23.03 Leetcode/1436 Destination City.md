---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/1436-destination-city/","tags":["dsa/hash"],"created":"2023-10-19T07:30:53.204-05:00","updated":"2023-10-19T07:32:27.079-05:00"}
---

# 1436 Destination City
## Problem Statement
Given an array of integers `nums` and an integer `target`, return _indices of the two numbers such that they add up to `target`_.
You may assume that each input would have **_exactly_ one solution**, and you may not use the _same_ element twice.
You can return the answer in any order.
**Input:** nums = [2,7,11,15], target = 9
**Output:** [0,1]
## Approach
The BF solution would be to compare each element with each other element and see if they match the target. This approach is very inefficient with a BigO(N²) due to two nested for loops. 
The recommended solution is to use a hashmap and check if target - current number is in the hashmap, if so return if not add the entry at i.
## Solution
```javascript
var twoSum = function(nums, target) {
    let hash = {}
    for (let i=0; i < nums.length; i++){
        if ((target - nums[i]) in hash){
            return [i, hash[target - nums[i]]]
        }
        hash[nums[i]] = i
    }
};
```
## Questions
## References
[LC](https://leetcode.com/problems/two-sum/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.01 Data Structures/Hash table\|Hash table]]