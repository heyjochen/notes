---
{"dg-publish":true,"permalink":"/1-software-engineering/languages/javascript/difference-between-map-and-objects/","tags":["type/permanent","code/javascript"],"created":"2023-07-20T07:10:54.968-05:00","updated":"2023-09-05T14:30:30.535-05:00"}
---

# Difference between Map and Objects
---
Map, a collection of keyed data items, accepts any type of key, whereas an object only accepts strings and converts keys to strings.

> [!Note]
> Don't use map[key] to access entries, as it would treat the map like an object with all its limitations. Always use .set(), .get()

Biggest benefit of a Map is that we can use Object as keys.

[Why would you use an Object as a key in a map?](https://stackoverflow.com/questions/60296652/what-is-a-practical-use-of-objects-as-keys-within-js-map-dataype)
Object, like DOM element, and you want to associate data with it, without modifying the data directly.