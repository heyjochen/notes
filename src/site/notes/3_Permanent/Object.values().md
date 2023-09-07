---
{"dg-publish":true,"permalink":"/3-permanent/object-values/","tags":["code/javascript"],"created":"2023-07-19T07:00:19.976-05:00","updated":"2023-09-05T14:35:28.846-05:00"}
---

# Object.values()

```javascript
const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.values(object1));
// Expected output: Array ["somestring", 42, false]
```

---
## Description
Returns the values in an array of each Object entry. This is the same as using a [[3_Permanent/for...in\|for...in]] loop.

## Parameters
obj

## Return Value
Array of the values of each entry in the passed object

## Example
I have used this method within the [[3_Permanent/Group Anagrams DSA\|Group Anagrams DSA]] problem, where I used it to return the previously created arrays of anagrams contained in a hashmap.

## References
- [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/values) 

## Related
[[3_Permanent/Group Anagrams DSA\|Group Anagrams DSA]]
[[3_Permanent/for...in\|for...in]]
[[3_Permanent/Object.keys()\|Object.keys()]]