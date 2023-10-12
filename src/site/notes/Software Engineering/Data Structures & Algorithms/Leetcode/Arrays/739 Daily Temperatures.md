---
{"dg-publish":true,"permalink":"/software-engineering/data-structures-and-algorithms/leetcode/arrays/739-daily-temperatures/","tags":["code/dsa"],"created":"2023-10-03T07:21:01.889-05:00","updated":"2023-10-04T08:07:38.671-05:00"}
---

# 739 Daily Temperatures
## Problem Statement
Given an array of integers `temperatures` represents the daily temperatures, return _an array_ `answer` _such that_ `answer[i]` _is the number of days you have to wait after the_ `ith` _day to get a warmer temperature_. If there is no future day for which this is possible, keep `answer[i] == 0` instead.

**Input:** temperatures = [73,74,75,71,69,72,76,73]
**Output:** [1,1,4,2,1,1,0,0]
## Approach
Using a **stack** to track the index of temperatures for which we have not found a higher temperature. Using **while** loop comparing temperatures and looking at stack to get the temperatures index. Using **results** array to reassign the difference of current i and index at result[index]. 
## Solution
```javascript
const dailyTemperatures = temperatures => {
	let stack = []
	let result = new Array(temperatures.length).fill(0)

	for (let i = 0; i < temperatures.length; i++) {
		while (stack.length && temperatures[i] > temperatures[stack[stack.length - 1]]) {
			const index = stack.pop()
			result[index] = i - index
		}
		stack.push(i)
	}
	return result
}
```
## Questions
- What is the purpose of the stack? What is it recording? When are we adding, when are we removing?
	Stack is used to track the temperatures for which we haven't found a higher temperature yet. We add after every for-loop iteration and pop while there is a smaller temperature than the current temperature on the stack. This also reassigns values in the results array.
	
- How is the loop functioning?
	Traditional for loop with while loop inside that verifies stack has content and temperature is bigger than temperature at top of stack
 
- How are we assigning elements in the output? Is it in order?
	No, they are reassigned by index and depend on which index is on the stack.
	
- How are we handling the last elements in the array?
	The loop will just run out of bounds
	
- What are monotonic stacks used for?
## References
[LC](https://leetcode.com/problems/daily-temperatures/)
[NC](https://www.youtube.com/watch?v=cTBiBSnjO3c)
## Related
[[Software Engineering/Data Structures & Algorithms/Data Structures/Monotonic Stack\|Monotonic Stack]]