---
{"dg-publish":true,"permalink":"/software-engineering/data-structures-and-algorithms/leetcode/strings/5-longest-palindromic-substring/","tags":["code/dsa"],"created":"2023-10-10T07:01:10.026-05:00","updated":"2023-10-11T06:35:56.283-05:00"}
---

# 5 Longest Palindromic Substring
## Problem Statement
Given a string `s`, return _the longest palindromic substring_ in `s`.

**Input:** s = "babad"
**Output:** "bab"
**Explanation:** "aba" is also a valid answer.
## Approach
**BF:** Loop through every character in the string, get all substrings and check for being palindrome. O(N * N2)
**Optimized:** We can use a center based approach where we expand via a helper function from each characters center outward. The expand happens via a while function respecting the bounds from our pointers (incoming indexes) and checking if the two characters are the same. If so we assign the sliced string to longest. At the end of every iteration we decrease the left pointer and increase the right pointer.
## Solution
```javascript
const longestPalindrome = (s) => {
  let longest = "";

  const expandAroundCenter = (l, r) => {
    while (l >= 0 && r < s.length && s[l] === s[r]) {
      if (r - l + 1 > longest.length) {
        longest = s.slice(l, r + 1);
      }
      l--;
      r++;
    }
  };

  for (let i = 0; i < s.length; i++) {
    expandAroundCenter(i, i); // Odd-length palindromes
    expandAroundCenter(i, i + 1); // Even-length palindromes
  }

  return longest;
};
```
## Questions
## References
[LC](https://leetcode.com/problems/longest-palindromic-substring/description/)
## Related
[[Software Engineering/Data Structures & Algorithms/Data Structures/Strings\|Strings]]
[[Software Engineering/Data Structures & Algorithms/Algorithms & Techniques/Two Pointers\|Two Pointers]]