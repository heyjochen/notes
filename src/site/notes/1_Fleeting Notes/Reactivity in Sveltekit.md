---
{"dg-publish":true,"permalink":"/1-fleeting-notes/reactivity-in-sveltekit/","created":"2023-07-23T22:30:13.958+02:00","updated":"2023-08-03T16:53:23.652+02:00"}
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

How is Reactivity triggered in Svelte?

---
## Related:
- [[3_Permanent Notes/Sveltekit MOC\|Sveltekit MOC]]