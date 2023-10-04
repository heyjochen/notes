---
{"dg-publish":true,"permalink":"/1-software-engineering/languages/swift/what-i-like-about-swift-and-swift-ui-compared-to-java-script-and-any-of-the-big-frameworks/","tags":["code/swift"],"created":"2023-09-30T19:11:39.652-05:00","updated":"2023-09-30T19:34:00.112-05:00"}
---

# What I like about Swift and SwiftUI compared to JavaScript and any of the big frameworks

1. How to implement a Search that searches across and Array of Persons
   ```Swift
   @State private var persons: [Person] = []
   @State private var searchTerm = ""

   var filteredPersons: [Person] {
	   guard !searchTerm.isEmpty else { return persons }
	   return persons.filter { $0.name.localizeCaseInsensitiveContains(searchTerm) }
   }
```

We start out with an array of persons, which has been fetched from an external data source and an empty searchField. We declare our computed property filteredPersons via a guard statement that returns the initial persons set whenever there is no character typed in, and otherwise loops over persons with a filter function and a closure. The $0 notation is a shorthand for a For Loop and represents each iteration of that For Loop. So for every person in the persons array we check the name.

This is a great example of a use-case for the guard statement, and also proof of how easy, concise and readable it is to filter an array of persons for a containing string.