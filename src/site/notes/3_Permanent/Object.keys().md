---
{"dg-publish":true,"permalink":"/3-permanent/object-keys/","created":"2023-07-21T05:50:59.821-06:00","updated":"2023-08-02T13:53:08.137-06:00"}
---

#code/method #code/javascript

# Object.keys()

```javascript
const obj = {
	a: 42,
	b: 43
}
for (let key of Object.keys(obj)) {
	console.log(key)
}
// a
// b
```

---
## Description
Loops over an Object and gives us access to the key.

## Parameters
Obj

## Return Value
An array of strings which represent the key of every object entry.
```javascript
const object1 = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.keys(object1));
// Expected output: Array ["a", "b", "c"]
```

## Example

## References
- [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)

## Related
