---
{"dg-publish":true,"permalink":"/3-permanent-notes/on-abstractions-in-software-engineering/"}
---

#type/permanent #code/best_practices

# On Abstractions in Software Engineering

> [!NOTE]
> The shallower and mundane our code is written, the easier it is to be maintained. There is no need for over-engineering something when there might be a simple solution available. Make it work and move on should be your mantra. If you do this, you will be able to build programs that run 24/7.
>
## Example
```javascript
function add(a, b) {
  return a + b;
}

function subtract(a, b) {
  return a - b;
}

// Example usage of the calculator functions
const num1 = 10;
const num2 = 5;

const sum = add(num1, num2);
console.log("Sum:", sum); // Output: Sum: 15

const difference = subtract(num1, num2);
console.log("Difference:", difference); // Output: Difference: 5
```
A simple calculator that abstracts the implementations of the add and subtract operations in their own functions. A user of the calculator would not need to know the implementation of those functions and could use them as is. Those functions provide a clear interface.

---
## Questions
- [[3_Permanent Notes/What is an abstraction?\|What is an abstraction?]] 
## Terms

## Related
- [[3_Permanent Notes/Best Practices MOC\|Best Practices MOC]]
## References