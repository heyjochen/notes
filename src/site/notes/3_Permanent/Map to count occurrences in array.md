---
{"dg-publish":true,"permalink":"/3-permanent/map-to-count-occurrences-in-array/","tags":["code/question","code/javascript"],"created":"2023-07-19T05:13:10.524-06:00","updated":"2023-09-05T13:34:45.988-06:00"}
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
[[3_Permanent/Top K Frequent Elements DSA\|Top K Frequent Elements DSA]]