---
{"dg-publish":true,"permalink":"/2-literature/system-design-process/","tags":["code/system_design"],"created":"2023-09-07T07:02:04.028-05:00","updated":"2023-09-08T06:02:55.573-05:00"}
---

# System Design Process
System Design is about finding technical solutions to abstract problems and can vary depending on problem we want to solve, therefore it is important to ask clarifying questions.
## Clarify requirements
Clarify requirements early to determine the exact scope of the problem we want to solve.
### Functional requirements
Base functionality that we need to provide to a user: 
- What are the features that we need to design for this system?
- What are the edge cases we need to consider, if any, in our design?
### Non-functional requirements
Non-behavioral requirements: Maintainability, reliability, scalability:
- Our requests should have minimal latency
- Our system needs to be highly available
### Extended requirements
Nice to have's, might be out of scope:
- Perfomance monitoring
- Metrics and analytics
## Estimations and constraints
What is the scale of the system we are implementing? Ask questions:
- How many users will this system have?
- How many read/write operations will it need to handle?
- How many requests per second?

That way we can think about how to scale such a system.
## API design
To better define our expectations for our system, we can think of our API interfaces. KISS:

`createUser(name: string, email: string): User`
## High-level component design
Design a basic diagram including system components like a [[Load Balancer\|Load Balancer]] and start discussing how the system will work from the client perspective.

- Is it best to design a monolithic or a microservices architecture?
- What type of database should we use?
## Detailed Design
Get into more details and show expertise, present different approaches, use existing experience and give examples. Don't be opinionated.

- What about load distribution?
- Should we use a cache?
- How will we handle a sudden spike in traffic?
## Identify and resolve bottlenecks
Think about bottlenecks. Read your companies blog and find out about their tech stack to get a sense of the problems they are facing.

- How can we make our system more robust?
- Is there a single point of failure?
## References
[Source](https://github.com/karanpratapsingh/system-design#system-design-interviews)
## Related