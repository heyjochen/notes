---
{"dg-publish":true,"permalink":"/3-permanent-notes/map-to-count-occurrences-in-array/","created":"2023-02-17 19:03","updated":"2023-08-03 16:51"}
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