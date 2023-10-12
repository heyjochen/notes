---
{"dg-publish":true,"permalink":"/software-engineering/languages/javascript/object-values/","tags":["code/javascript"],"created":"2023-07-19T07:00:19.976-05:00","updated":"2023-10-05T06:45:19.661-05:00"}
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
Returns the values in an array of each Object entry. This is the same as using a [[Software Engineering/Languages/for...in\|for...in]] loop.

## Parameters
obj

## Return Value
Array of the values of each entry in the passed object

## Example
I have used this method within the [[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/49 Group Anagrams\|49 Group Anagrams]] problem, where I used it to return the previously created arrays of anagrams contained in a hashmap.

## References
- [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/values) 

## Related
[[Software Engineering/Data Structures & Algorithms/Leetcode/Arrays/49 Group Anagrams\|49 Group Anagrams]]
[[Software Engineering/Languages/for...in\|for...in]]
[[Software Engineering/Languages/Javascript/Object.keys()\|Object.keys()]]