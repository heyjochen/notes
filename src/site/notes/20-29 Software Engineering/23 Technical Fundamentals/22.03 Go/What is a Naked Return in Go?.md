---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/22-03-go/what-is-a-naked-return-in-go/","created":"2023-08-04T07:54:42.225-05:00","updated":"2023-08-04T07:59:09.552-05:00"}
---

#type/permanent #code/go

---
First, a naked return should only used in very short functions. 
Return values in go can be named: `(x, y int)` , then a return statement without arguments would return the named return values. This would look like so:

```go
func split(sum in) (x, y int) {
	x = sum * 2
	y = x - 4
	return
}
```
---
## Questions
## Terms
## References
[Tour of Go](https://go.dev/tour/basics/7)
## Related