---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-03-leetcode/242-valid-anagram/","tags":["dsa/string"],"created":"2023-07-24T06:13:30.199-05:00","updated":"2023-10-17T07:56:50.227-05:00"}
---

# 242 Valid Anagram
## Problem Statement
Given two strings `s` and `t`, return `true` _if_ `t` _is an anagram of_ `s`_, and_ `false` _otherwise_.
An **Anagram** is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

**Input:** s = "anagram", t = "nagaram"
**Output:** true
## Approach
- Create a Hashmap for characters
- Loop through the string, grab left and right Char. 
- For Left char we either increase or set to 1, For Right Char we either decrease or set to -1.
- One final for...in loop through hashmap keys, if their value isn't 0 return false, otherwise outside of loop return true
## Solution
```javascript
const isAnagram = (s, t) => {
    if (s.length !== t.length) return false;

    let charCount = {};

    for (let i = 0; i < s.length; i++) {
        const charS = s[i];
        const charT = t[i];

        charCount[charS] = charCount[charS] ? charCount[charS] + 1 : 1;
        charCount[charT] = charCount[charT] ? charCount[charT] - 1 : -1;
    }

    for (let key in charCount) {
        if (charCount[key] !== 0) {
            return false;
        }
    }

    return true;
};
```
## Questions
- If using a hashmap to check if two words are anagrams, what would be the keys and the values in the hashmap?
## References
- [LC](https://leetcode.com/problems/valid-anagram/)
## Related
[[DSA MOC\|DSA MOC]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/for...in\|for...in]]
[[Hashmap\|Hashmap]]