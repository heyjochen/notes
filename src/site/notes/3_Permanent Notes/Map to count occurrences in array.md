---
{"dg-publish":true,"permalink":"/3-permanent-notes/map-to-count-occurrences-in-array/","created":"2023-07-19T13:13:10.524+02:00","updated":"2023-08-03T23:51:02.309+02:00"}
---

#code/question #code/javascript

# Map to count occurrences in array

```javascript
for (let num of nums) {
  freqMap.set(num, (freqMap.get(num) || 0) + 1);
}
```

---
## References

## Related
[[3_Permanent Notes/Top K Frequent Elements DSA\|Top K Frequent Elements DSA]]