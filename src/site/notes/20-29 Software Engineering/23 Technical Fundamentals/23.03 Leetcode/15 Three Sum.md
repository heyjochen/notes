---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/15-three-sum/","tags":["dsa/array"],"created":"2023-07-25T06:56:31.693-05:00","updated":"2023-10-17T07:54:42.054-05:00"}
---

# 15 Three Sum
## Problem Statement
Given an integer array nums, return all the triplets `[nums[i], nums[j], nums[k]]` such that `i != j`, `i != k`, and `j != k`, and `nums[i] + nums[j] + nums[k] == 0`.

Notice that the solution set must not contain duplicate triplets.
**Input:** nums = [-1,0,1,2,-1,-4]
**Output:** [[-1,-1,2],[-1,0,1\|-1,-1,2],[-1,0,1]]
## Approach
We solve this with a two pointers approach where we sort our input immediately. We then loop over the whole array and create our pointers as well as a sum. Next we traverse the array within the bounds of our pointers and build the sum which gets evaluated. Afterwards we need to check for duplicates
## Solution
```javascript
const threeSum = (arr) => {
  let results = [];

  arr.sort((a, b) => a - b);
  for (let i = 0; i < arr.length - 2; i++) {
    if (i > 0 && arr[i] === arr[i - 1]) {
      continue;
    }

    let left = i + 1,
      right = arr.length - 1;

    while (left < right) {
      const currentSum = arr[i] + arr[left] + arr[right];

      if (currentSum === 0) {
        results.push([arr[left], arr[right], arr[i]]);
        left++;
        right--;

        while (left < right && arr[left] === arr[left - 1]) {
          left++;
        }

        while (left < right && arr[right] === arr[right + 1]) {
          right--;
        }
      } else if (currentSum < 0) {
        left++;
      } else {
        right--;
      }
    }
  }

  return results;
};
```
## Gotcha
- .[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/sort()\|sort()]] mutates the original array 
- I only check for duplicates when I found a valid sum or after every loop iteration
## Questions
1. How does sorting help?
	We usually want to find pairs or triplets. If an input array is sorted, they are close to each other. Also its easier to avoid duplicates as they are adjacent. So we could use an if statement that checks if the current value is the same as previous and if so skip it.
2. How do we ensure no duplicate triplets?
	When we check if the sum === 0, we have two additional while loops that check if the adjacent pointer elements are the same.
3. Why are we choosing a nums[i], nums[left], and nums[right] pointer?
	We are using three different pointers, starting with the first potential number in the triplet. The left pointer represents the second element of the triplet, and will move forward to explore larger values. The right pointer represents the third element of the triplet, and will move backward to explore smaller values.
4. What does shifting the L / R pointer mean?
	L: Increase sum, R: Decrease sum (remember the array is sorted)
5. What happens if the current value (nums[i]) is the same as before?
	Shift the L pointer again.
6. What happens when the sum is zero?
	We push the array containing nums[i], nums[left], nums[right] into result, then check if the pointers are equal to the next value in the array, if so shift with a while loop. Otherwise just shift once.
## References
[LC](https://leetcode.com/problems/3sum/)
## Related
[[DSA MOC\|DSA MOC]]
[[20-29 Software Engineering/23 Technical Fundamentals/23.03 Leetcode/167 Two Sum II\|167 Two Sum II]]