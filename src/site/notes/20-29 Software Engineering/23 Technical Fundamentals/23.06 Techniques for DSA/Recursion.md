---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-06-techniques-for-dsa/recursion/","tags":["code/dsa/technique"],"created":"2023-10-24T06:55:42.497-05:00","updated":"2023-10-24T07:44:17.706-05:00"}
---

# Recursion
Recursion is a way of solving a problem by breaking it down into smaller subproblems.
A recursive function MUST have one or more base cases otherwise it will go on forever.

## Example
Calculate the factorial of a number n.
```Javascript
function factorial(n) {
	if (n === 1) return 1
	return n * factorial(n-1)
}
```
This function has a base case defined and calls itself until it meets this base case. If we want to walk trough the code to see what it does we would:
1. Identify the base case
2. Walk through the function for the base case
3. Do the same for the remaining cases

By doing this you will see that behind the scenes recursion is implemented via a Stack onto which the currently called function gets pushed.
## References
## Related