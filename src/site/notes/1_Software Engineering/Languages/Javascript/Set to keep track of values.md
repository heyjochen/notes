---
{"dg-publish":true,"permalink":"/1-software-engineering/languages/javascript/set-to-keep-track-of-values/","tags":["code/question","code/javascript"],"created":"2023-07-19T06:15:40.097-05:00","updated":"2023-10-05T07:10:10.405-05:00"}
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
- [[1_Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/347 Top K Frequent Elements\|347 Top K Frequent Elements]]