---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-02-algorithms/depth-first-traversal/","created":"2023-12-13T06:07:04.035-06:00","updated":"2023-12-13T08:46:55.371-06:00"}
---

# Depth-First Traversal

>[!Def]
>  Depth-First Traversal is a graph traversal algorithm to visit all vertices or edges in a Graph or Tree. Doing a DFS means going as deep as we can first.

```javascript
function inorderTraversal(node) {
  if (node === null) return;
  inorderTraversal(node.left);
  console.log(node.val);
  inorderTraversal(node.right);
}
```

