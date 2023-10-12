---
{"dg-publish":true,"permalink":"/software-engineering/languages/javascript/set-in-java-script/","tags":["type/permanent","code/javascript"],"created":"2023-07-17T16:57:49.240-05:00","updated":"2023-09-05T18:20:36.037-05:00"}
---

# Set in JavaScript
A Set in JavaScript keeps track of values and only stores unique values. 

```javascript
const arr = [0,1,1,1,2,3]
const set = new Set([...arr])
console.log(set)
```

Sets are great to keep track of active Filter Badges or of loading / fetching states when making requests to external data sources.

## Methods
### add()
Adds an entry in a Set and takes the entry as argument
### delete()
Removes a specified entry from the Set
### has()
Returns a boolean depending on the value existing or not in the Set
 
---
##### Questions
- How can you get the size / length of a set?
  .size property returns the amount of unique elements of each Set.
- How is the performance compared to an array?

##### Terms
<!-- Links to definition pages -->

##### References
<!-- Links to pages not referenced in the content -->