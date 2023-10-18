---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/22-02-java-script/object-values/","tags":["code/javascript"],"created":"2023-07-19T07:00:19.976-05:00","updated":"2023-10-05T06:45:19.661-05:00"}
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
Returns the values in an array of each Object entry. This is the same as using a [[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/for...in\|for...in]] loop.

## Parameters
obj

## Return Value
Array of the values of each entry in the passed object

## Example
I have used this method within the [[20-29 Software Engineering/23 Technical Fundamentals/23.03 Leetcode/49 Group Anagrams\|49 Group Anagrams]] problem, where I used it to return the previously created arrays of anagrams contained in a hashmap.

## References
- [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/values) 

## Related
[[20-29 Software Engineering/23 Technical Fundamentals/23.03 Leetcode/49 Group Anagrams\|49 Group Anagrams]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/for...in\|for...in]]
[[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Object.keys()\|Object.keys()]]