---
{"dg-publish":true,"permalink":"/3-permanent/what-is-the-fmt-package/","created":"2023-08-03T06:22:15.901-06:00","updated":"2023-08-16T13:56:57.886-06:00"}
---

#type/permanent 

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