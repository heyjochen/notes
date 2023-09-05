---
{"dg-publish":true,"permalink":"/3-permanent/map-in-java-script/","tags":["type/permanent","code/javascript"],"created":"2023-07-17T15:43:45.800-06:00","updated":"2023-09-05T13:34:31.681-06:00"}
---

# Map in JavaScript

A Map in JavaScript let's us keep track of values. Each entry in a map has a key and a value. An ideal use-case: [[3_Permanent/Map to count occurrences in array\|Map to count occurrences in array]]
Above snippet will create an entry for num, tries to look up if there is already an entry, if so increases that value by 1, if no entry, create one set it to 0 and increase by 1.

## Methods
### set(key, value)
Takes two arguments, the key and the value, and creates or updates an entry in the Map.

### get(key)
Takes one argument which has to reference the key we want to get and returns the element.

### has(key)
Takes one argument which has to reference the key we want to get and returns a boolean if it exists.

---
##### Questions
- [[3_Permanent/How can we loop over the entries in a map and extract key and value of each entry?\|How can we loop over the entries in a map and extract key and value of each entry?]]?

##### Terms
<!-- Links to definition pages -->

##### References
<!-- Links to pages not referenced in the content -->
- [[Hashmap\|Hashmap]]
