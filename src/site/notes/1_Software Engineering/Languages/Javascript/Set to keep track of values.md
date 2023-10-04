---
{"dg-publish":true,"permalink":"/1-software-engineering/languages/javascript/set-to-keep-track-of-values/","tags":["code/question","code/javascript"],"created":"2023-07-19T06:15:40.097-05:00","updated":"2023-09-05T14:40:16.814-05:00"}
---

# Set to keep track of values

```javascript
for (let [num, freq] of freqMap) {
	bucket[freq] = (bucket[freq] || new Set()).add(num);
}
```

---

## References
- 

## Related
- [[1_Software Engineering/Data Structures & Algorithms/Leetcode/Top K Frequent Elements DSA\|Top K Frequent Elements DSA]]