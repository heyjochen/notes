---
{"dg-publish":true,"permalink":"/2-literature/how-to-do-great-code-reviews/","tags":["type/literature","source/blog"],"created":"2023-08-14T22:41:33.499-05:00","updated":"2023-09-05T14:27:36.163-05:00"}
---

# How to do great Code Reviews?

> [!NOTE] Info
> This is a summary of different blog posts related to Best practices around Code Reviews by Molly King.

There are three parts of a Code Review:
1. You review your own code before you create a PR
2. You review someone else's code after they created a PR
3. You have your code reviewed by someone else
### Reviewing your own code
Always run your code and make sure it works before you create a PR. Make use of linters to adhere to your teams' standard. Read through the diffs that you created and compare your changes to the ticket you worked on. Do they cover everything or do the go beyond? If so, maybe split the work up into an additional PR. Are your variables and function names properly named? At some point in the future someone else will have to take care of your code.
### Reviewing someone else's code
- Be empathic with your colleagues' code
- Be sensitive
- Something might seem simple to you but that doesn't mean that it is obvious to them, so make sure to provide additional information. Avoid filler words of just / simply
- Prefer writing open ended questions over demands.
- Focus on sharing knowledge through Code Reviews
- Keep a positive attitude
- Treat reviews as a teaching opportunity
### Having your code being reviewed
- You are not your code. Don't have too much ego and take critique personally
- Clarify and communicate
- Address pointed out issues
 
---
## Questions
## Terms
- Empathy
- Sensitivity
- Ego
## References
[Better Code Review, Part One](https://engineering.ziffmedia.com/better-code-review-part-one-ae3d4ff0494d)
[Better Code Review, Part Two](https://medium.com/ziffmedia-engineering/better-code-review-part-two-92f17ee42c56)
[Better Code Review, Part Three](https://engineering.ziffmedia.com/better-code-review-part-3-4efb568885)
[Frustration Free Code-Reviews](https://adavis.info/2018/09/frustration-free-code-reviews.html)
## Related
[[3_Permanent/Best Practices MOC\|Best Practices MOC]]
[[3_Permanent/On Empathy in Software Engineering\|On Empathy in Software Engineering]]