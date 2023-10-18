---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/22-02-java-script/map-in-java-script/","tags":["type/permanent","code/javascript"],"created":"2023-07-17T16:43:45.800-05:00","updated":"2023-09-05T18:20:51.038-05:00"}
---

# Map in JavaScript
A Map in JavaScript let's us keep track of values. Each entry in a map has a key and a value. An ideal use-case: [[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/Map to count occurrences in array\|Map to count occurrences in array]]
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
- [[20-29 Software Engineering/23 Technical Fundamentals/22.02 JavaScript/How can we loop over the entries in a map and extract key and value of each entry?\|How can we loop over the entries in a map and extract key and value of each entry?]]?

##### Terms
<!-- Links to definition pages -->

##### References
<!-- Links to pages not referenced in the content -->
- [[Hashmap\|Hashmap]]
