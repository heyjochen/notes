---
{"dg-publish":true,"permalink":"/20-29-software-engineering/23-technical-fundamentals/23-07-react/error-is-of-type-unknown/","created":"2023-12-13T08:43:39.221-06:00","updated":"2023-12-13T08:46:34.783-06:00"}
---

# Error is of type unknown
This is a typescript related error that came up in the catch block. To avoid it we can include a if statement that checks for the instanceof Error

```javascript
} catch (error) {
	if (error instanceof Error) {
		alert(error.message)
	}
}
```
