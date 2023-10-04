---
{"dg-publish":true,"permalink":"/1-software-engineering/languages/javascript/map-to-count-occurrences-in-array/","tags":["code/question","code/javascript"],"created":"2023-07-19T06:13:10.524-05:00","updated":"2023-09-05T14:34:45.988-05:00"}
---

# Map to count occurrences in array

```javascript
for (let num of nums) {
  freqMap.set(num, (freqMap.get(num) || 0) + 1);
}
```

---
## References

## Related
[[1_Software Engineering/Data Structures & Algorithms/Leetcode/Top K Frequent Elements DSA\|Top K Frequent Elements DSA]]