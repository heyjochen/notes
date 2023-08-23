---
{"dg-publish":true,"permalink":"/3-permanent-notes/set-to-keep-track-of-values/","created":"2023-07-19T06:15:40.097-05:00","updated":"2023-08-02T14:53:00.558-05:00"}
---

#code/question #code/javascript

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
- [[3_Permanent Notes/Top K Frequent Elements DSA\|Top K Frequent Elements DSA]]