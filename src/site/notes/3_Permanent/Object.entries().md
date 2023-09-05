---
{"dg-publish":true,"permalink":"/3-permanent/object-entries/","created":"2023-07-21T05:43:02.476-06:00","updated":"2023-08-02T13:53:05.761-06:00"}
---

#code/method #code/javascript

# Object.entries()

```javascript
const obj = {
	a: 42,
	b: 43
}
for (let [key, value] of Object.entries(obj)) {
	console.log(key, value)
}
// a, 42
// b, 43
```

---
## Description
Loops over an Object and gives us access to every single entry. Can be used to destructure key and value

## Parameters
Obj

## Return Value
An array of arrays consisting of the key, value pairs.
```javascript
const obj = { foo: "bar", baz: 42 };
console.log(Object.entries(obj)); // [ ['foo', 'bar'], ['baz', 42] ]
```

## Example

## References
- [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries)

## Related
