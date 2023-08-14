---
{"dg-publish":true,"permalink":"/3-permanent-notes/difference-between-map-and-objects/","created":"2023-07-20T14:10:54.968+02:00","updated":"2023-08-03T15:09:25.475+02:00"}
---

#type/permanent #code/javascript 

---
Map, a collection of keyed data items, accepts any type of key, whereas an object only accepts strings and converts keys to strings.

> [!Note]
> Don't use map[key] to access entries, as it would treat the map like an object with all its limitations. Always use .set(), .get()

Biggest benefit of a Map is that we can use Object as keys.

[Why would you use an Object as a key in a map?](https://stackoverflow.com/questions/60296652/what-is-a-practical-use-of-objects-as-keys-within-js-map-dataype)
Object, like DOM element, and you want to associate data with it, without modifying the data directly.