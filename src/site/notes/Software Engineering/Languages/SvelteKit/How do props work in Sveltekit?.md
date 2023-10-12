---
{"dg-publish":true,"permalink":"/software-engineering/languages/svelte-kit/how-do-props-work-in-sveltekit/","tags":["code/sveltekit","type/permanent"],"created":"2023-08-03T09:49:49.238-05:00","updated":"2023-09-05T14:32:44.675-05:00"}
---

# How do props work in Sveltekit?
---
When we intend to pass props from a parent component to a child we need to declare the passed prop within the child component with the export keyword:
```javascript
<script>
	export let answer;
</script>
```
---
## Questions
## Terms
## Related
[[Sveltekit MOC\|Sveltekit MOC]]
## References