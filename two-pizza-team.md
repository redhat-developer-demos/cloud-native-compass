# Two pizza team

The term "Two pizza team" comes from Amazon and describes a team size such that it is the number of people that can be fed by two pizzas. The reality is that the term is not only a reference to team size but, rather, underscores the concept of "Accountability".

In the world of Cloud Native Computing, a small team is responsible for an application and its life, from inception to coding to support (some people make an exception for security, which may be handled by a central security team for the sake of consistency and completeness). In traditional (e.g. waterfall) SDLC schemes, teams are built around the division of responsibilities: Design, development, testing, database, operations, etc.

In the microservices model, teams are built around a function or unit of work: Adding to inventory, retrieving a list of nearby stores, etc. This typically small team is free to design, develop, test and deploy the microservice as it sees fit. Language choice (Java, C#, Go, etc.) is not governed by an outside management force, but is determined by the team's skill set or a particular language's best fit for a function.

The application design is determined by the team; any local database is their choice as well, as it is deployed with the solution. Likewise, testing remains their challenge, with a built-in incentive: The team also supports the application, so fewer defects means less time spent in support. On the other hand, a problem at 3AM on a Saturday is the team's responsibility and theirs alone.
