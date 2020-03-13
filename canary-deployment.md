# Canary Deployment

A deployment pattern where a new version is eased into production by making it available to a given to an increasingly-larger subset of users, until it either reaches 100 percent of the audience or is deemed not ready and is abandoned (and the audience percentage is set to zero).

By using intelligent routing, such as that provided by istio [istio.io], it is possible to direct web requests to a service based on user-defined criteria, such as geographical location, user id, etc. With that functionality it becomes possible to split traffic to an existing version and a new, Canary version.

The term “Canary” in this context refers to the old idea of carrying a canary in a cage into a coal mine, using it as a snapshot of the mine’s conditions. If, for example, the canary died, it meant a buildup of dangerous gases such as carbon monoxide. This signaled to the miners that conditions were life-threatening and it was time to exit the mine.

In software, a Canary Deployment allows you to monitor the success of a new version -- performance, correctness, robustness, etc -- with a small audience. Based on success or failure of the application, the user base is then either slowly expanded until 100 percent of the users are using the new version, or scaled back to zero and the application terminated.
