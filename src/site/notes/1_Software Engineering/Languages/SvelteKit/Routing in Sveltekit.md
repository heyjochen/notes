---
{"dg-publish":true,"permalink":"/1-software-engineering/languages/svelte-kit/routing-in-sveltekit/","tags":["code/sveltekit"],"created":"2023-07-24T15:04:05.418-05:00","updated":"2023-10-04T07:21:59.243-05:00"}
---

# Routing in Sveltekit

Routing in Svelte is file based, meaning that if we want to have a /about route, we will create a folder about in our root with a file +page.svelte.

We can have a common layout for each route, which will be in +layout.svelte.
We can make use of [[1_Software Engineering/Languages/SvelteKit/Slot\|Slot]].
We can also use +page.server.ts to handle loading of data.

---
## Related:
- [[Sveltekit MOC\|Sveltekit MOC]]
- [[1_Software Engineering/Languages/SvelteKit/Route Parameters in Sveltekit\|Route Parameters in Sveltekit]]