---
{"dg-publish":true,"permalink":"/3-permanent-notes/reactivity-in-sveltekit/","created":"2023-07-23T15:30:13.958-05:00","updated":"2023-08-14T23:30:42.030-05:00"}
---

#code/sveltekit

---
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
- [[3_Permanent Notes/Sveltekit MOC\|Sveltekit MOC]]