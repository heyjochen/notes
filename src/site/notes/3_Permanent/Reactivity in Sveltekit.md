---
{"dg-publish":true,"permalink":"/3-permanent/reactivity-in-sveltekit/","tags":["code/sveltekit"],"created":"2023-07-23T14:30:13.958-06:00","updated":"2023-09-05T13:39:22.526-06:00"}
---

# Reactivity in Sveltekit
Reactivity happens through assignments. 
Reactive Declarations are indicated by the $ sign. They become valuable when you need to reference them multiple times or when they depend on other reactive values.

```javascript
	let count = 1
	$: doubled = count * 2
```

Not only limited to reactive values, we can also have reactive statement

```javascript
	$: if (count > 2) {
		alert('count too high')
		count = 0
	}
```

---
## Related:
- [[3_Permanent/Sveltekit MOC\|Sveltekit MOC]]