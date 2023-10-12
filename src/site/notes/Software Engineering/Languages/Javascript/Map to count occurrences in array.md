---
{"dg-publish":true,"permalink":"/software-engineering/languages/javascript/map-to-count-occurrences-in-array/","tags":["code/question","code/javascript"],"created":"2023-07-19T06:13:10.524-05:00","updated":"2023-10-05T07:10:10.399-05:00"}
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
[[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/347 Top K Frequent Elements\|347 Top K Frequent Elements]]