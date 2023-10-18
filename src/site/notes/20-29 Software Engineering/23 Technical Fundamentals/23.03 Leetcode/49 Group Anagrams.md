---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/49-group-anagrams/","tags":["dsa/array"],"created":"2023-07-19T06:36:38.044-05:00","updated":"2023-10-17T07:53:27.992-05:00"}
---

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
[[DSA MOC\|DSA MOC]]
[[charCodeAt\|charCodeAt]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Object.values()\|Object.values()]]