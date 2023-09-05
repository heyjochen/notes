---
{"dg-publish":true,"permalink":"/3-permanent/for-in/","tags":["code/method","code/javascript"],"created":"2023-07-21T05:56:21.837-06:00","updated":"2023-09-05T13:30:57.435-06:00"}
---

# for...in

```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// Expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```

---
## Description
The for...in loop is a loop in JavaScript that **iterates** over all *enumerable string properties* of an object.

## Parameters
variable, object, statement
```javascript
for (variable in object)
  statement
```

## Gotcha
Even though the `for...in` works to loop over an array we should use a traditional for-loop, a forEach() or `for...of`. As Arrays are just objects in JavaScript it would also loop over properties inherited from the prototype chain. It is also less performant.

---
## References
- [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)

## Related
