---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/832-flipping-an-image/","tags":["code/dsa/two_pointers"],"created":"2023-11-08T07:07:35.349-06:00","updated":"2023-11-08T07:10:36.353-06:00"}
---

# 832 Flipping an Image
## Problem Statement
Given an `n x n` binary matrix `image`, flip the image **horizontally**, then invert it, and return _the resulting image_.

To flip an image horizontally means that each row of the image is reversed.
- For example, flipping `[1,1,0]` horizontally results in `[0,1,1]`.
To invert an image means that each `0` is replaced by `1`, and each `1` is replaced by `0`.
- For example, inverting `[0,1,1]` results in `[1,0,0]`.

**Input:** image = [[1,1,0],[1,0,1],[0,0,0\|1,1,0],[1,0,1],[0,0,0]]
**Output:** [[1,0,0],[0,1,0],[1,1,1\|1,0,0],[0,1,0],[1,1,1]]
## Approach
Loop through the array, init two pointers, one at the beginning, one at the end, whiile loop through, swap position and invert via 1 -
## Solution
```javascript
var flipAndInvertImage = function(image) {
	for (const img of image) {
		let l = 0,
			r = img.length - 1
		while (l <= r) {
			[img[l], img[r]] = [1 - img[r], 1 - img[l]];
			l++
			r--
		}
	}
  
	return image
};
```
## Questions
## References
[LC](https://leetcode.com/problems/flipping-an-image/description/)
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.06 Techniques for DSA/Two Pointers\|Two Pointers]]