---
{"dg-publish":true,"permalink":"/3-permanent-notes/routing-in-sveltekit/","created":"2023-05-24 20:31","updated":"2023-08-02 14:49"}
---

#code/sveltekit

# Routing in Sveltekit

Routing in Svelte is file based, meaning that if we want to have a /about route, we will create a folder about in our root with a file +page.svelte.

We can have a common layout for each route, which will be in +layout.svelte.
We can make use of [[3_Permanent Notes/Slot in Sveltekit\|Slot in Sveltekit]].
We can also use +page.server.ts to handle loading of data.

---
## Related:
- [[3_Permanent Notes/Sveltekit MOC\|Sveltekit MOC]]
- [[3_Permanent Notes/Route Parameters in Sveltekit\|Route Parameters in Sveltekit]]