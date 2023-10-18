---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/22-03-go/what-is-the-relationship-between-packages-and-modules/","tags":["code/go"],"created":"2023-08-04T07:15:37.177-05:00","updated":"2023-10-04T07:20:16.026-05:00"}
---

# What is the relationship between packages and modules in Go?
Go code is grouped into packages, and packages are grouped into modules.
### Packages
There are two types of packages:
1. Library packages - Imported via their path and don't have a func main(), are intended to be used as dependencies by other programs/packages
2. Executable packages - Have the func main() and package main

Here is an example of a package called greetings.go that can be called from another package, takes in a string and returns a greeting:
```go
package greetings

import "fmt"

func Hello(name string) string {
	message := fmt.Sprintf("Hi, %v. Welcome!", name)
	return message
}
```

Then in our executable we would call it:
```go
package main

import (
	"fmt"
	"example.com/greetings"
)

func main() {
	message := greetings.Hello("Gladys")
	fmt.Println(message)
}
```
### Modules
A module is a collection of related packages versioned together. A module is *defined* by a go.mod file where it specifies its name and version as well as the dependencies and their versions to stay consistent between builds.
```go
module github.com/username/myproject

go 1.20

require (
    github.com/someuser/somepackage v1.2.3
    github.com/otheruser/otherpackage v0.1.0
)
```

---
## Questions
- Is there something similar to this concept in JavaScript?
	- Yes: exported functions that modularize code, and package.json to track dependencies 
## Terms
## Related
[[20-29 Software Engineering/23 Technical Fundamentals/22.03 Go/What is the purpose of a module?\|What is the purpose of a module?]]
[[How can we call a function that is within another module?\|How can we call a function that is within another module?]]
## References
[Using Go Modules](https://go.dev/blog/using-go-modules)