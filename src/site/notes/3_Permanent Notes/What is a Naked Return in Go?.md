---
{"dg-publish":true,"permalink":"/3-permanent-notes/what-is-a-naked-return-in-go/","created":"2023-08-04T14:54:42.225+02:00","updated":"2023-08-04T14:59:09.552+02:00"}
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