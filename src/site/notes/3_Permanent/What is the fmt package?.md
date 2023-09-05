---
{"dg-publish":true,"permalink":"/3-permanent/what-is-the-fmt-package/","tags":["type/permanent"],"created":"2023-08-03T06:22:15.901-06:00","updated":"2023-09-05T13:44:47.671-06:00"}
---

# What is the fmt package?

Used for formatting input and output similar to C's printf and scanf.

Print a Line:
```go
func main() {
    fmt.Println("Hello, Go!")
}
```

Read Input:
```go
func main() {
    var inputString string
    fmt.Print("Enter your name: ")
    fmt.Scan(&inputString)
    fmt.Println("Hello, " + inputString + "!")
}
```
 
---
## Questions
## Terms

## References

## Related