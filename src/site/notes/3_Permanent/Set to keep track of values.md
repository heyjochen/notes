---
{"dg-publish":true,"permalink":"/3-permanent/set-to-keep-track-of-values/","tags":["code/question","code/javascript"],"created":"2023-07-19T05:15:40.097-06:00","updated":"2023-09-05T13:40:16.814-06:00"}
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
- [[3_Permanent/Top K Frequent Elements DSA\|Top K Frequent Elements DSA]]