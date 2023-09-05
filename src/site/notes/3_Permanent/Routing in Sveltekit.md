---
{"dg-publish":true,"permalink":"/3-permanent/routing-in-sveltekit/","tags":["code/sveltekit"],"created":"2023-07-24T14:04:05.418-06:00","updated":"2023-09-05T13:39:50.870-06:00"}
---

# Routing in Sveltekit

Routing in Svelte is file based, meaning that if we want to have a /about route, we will create a folder about in our root with a file +page.svelte.

We can have a common layout for each route, which will be in +layout.svelte.
We can make use of [[3_Permanent/Slot in Sveltekit\|Slot in Sveltekit]].
We can also use +page.server.ts to handle loading of data.

---
## Related:
- [[3_Permanent/Sveltekit MOC\|Sveltekit MOC]]
- [[3_Permanent/Route Parameters in Sveltekit\|Route Parameters in Sveltekit]]