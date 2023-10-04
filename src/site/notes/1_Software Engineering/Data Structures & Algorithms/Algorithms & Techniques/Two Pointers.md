---
{"dg-publish":true,"permalink":"/1-software-engineering/data-structures-and-algorithms/algorithms-and-techniques/two-pointers/","tags":["code/javascript","code/dsa/technique"],"created":"2023-09-14T06:11:45.889-05:00","updated":"2023-10-04T07:51:45.102-05:00"}
---

# Two Pointers
Used with certain patterns revolving around arrays, often times sorted, or in combination with a sliding window. Also to check for a palindrome, or reversing.
## Use Cases:
- Searching: Finding elements or patterns
- Sorting: Rearranging elements in specific order
- Sliding Window
## Common Questions:
- Two Sum
- [[1_Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/167 Two Sum II\|167 Two Sum II]]
- Three Sum
- Sliding Window
## Steps:
- Init the pointers
- Loop through the DS according to requirements
- Update the pointers based on requirements
- Return when pointers or satisfy problem's logic
## Two Sum
> Given an array of sorted numbers and a target sum, find a pair in the array whose sum is equal to the given target.

We could BF it by looking at each element and compare it with the rest, but that would put our Big O into N². 
## How to get from O(N²) to O(N)?
As we know that our input array is sorted we can introduce a L and R Pointer and use them to move through the array. If arr[L] + arr[R] > target then reduce R pointer, otherwise increase L pointer.
## What loop are we using?
While loop as the two Pointers, L and R, move towards each other and.
```javascript
while (L < R) { }
```
## Problem Statement
> Given an array of sorted numbers and a target sum, find a pair in the array whose sum is equal to the given target.
> 
> Write a function to return the indices of the two numbers (i.e. the pair) such that they add up to the given target.

`Input: [2, 5, 9, 11], target=11
`Output: [0, 2]
`Explanation: The numbers at index 0 and 2 add up to 11: 2+9=11

``` javascript
const targetSum = (arr, target) => {
	let left = 0,
		right = arr.length - 1

	while (left < right) {

		// can be improved by making variable sum
		if (arr[left] + arr[right] === target) {
			return [left, right]
		}
		
		if (arr[left] + arr[right] > target) {
			right--
		} else {
			left++
		}
	}
	return [-1, -1]
}
```
## Alternate Approach
This can also be solved with a hashmap, which also works with non-sorted arrays.
## References
## Related
[LC](https://leetcode.com/tag/two-pointers/)