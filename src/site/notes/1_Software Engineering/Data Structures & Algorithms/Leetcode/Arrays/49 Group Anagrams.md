---
{"dg-publish":true,"permalink":"/1-software-engineering/data-structures-and-algorithms/leetcode/arrays/49-group-anagrams/","created":"2023-07-19T06:36:38.044-05:00","updated":"2023-10-05T07:38:00.142-05:00"}
---

#code/question #code/javascript #code/dsa
# 49 Group Anagrams
## Problem Statement
Given an array of strings `strs`, group **the anagrams** together. You can return the answer in **any order**.
An **Anagram** is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

**Input:** strs = ["eat","tea","tan","ate","nat","bat"]
**Output:** [["bat"],["nat","tan"],["ate","eat","tea"\|"bat"],["nat","tan"],["ate","eat","tea"]]
## Approach
We loop over each string in the input array. Within our loop we create an array that is of length 26 and fill it with 0's. This is being used to keep track of every character in each string, that way we are able to keep track of anagrams. This array is then being used within a hashmap where it will serve as the key to set up an entry that equals the [...str].
## Solution
```javascript
const groupAnagrams = strs => {
	let map = {}

	for (let str of strs){
		const arr = new Array(26).fill(0)

		for (let char of str) {
			arr[char.charCodeAt() - 97]++
		}

		let count = arr.join('.')
		map[count] ? map[count].push(str) : map[count] = [str]
	}
	return Object.values(hash)
}
```
## Gotcha

## Questions
- How do you populate the array to keep track of individual characters?
- How do we add an entry in the hashmap once looped through the string?
## References
[LC](https://leetcode.com/problems/group-anagrams/description/) 
## Related
[[1_Software Engineering/MOCs/DSA MOC\|DSA MOC]]
[[charCodeAt\|charCodeAt]]
[[1_Software Engineering/Languages/Javascript/Object.values()\|Object.values()]]