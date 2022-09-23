# A/B Testing

A/B testing is an approach to testing a hypothesis by creating a control group and introducing variant scenarios, functionality, appearance, et. al.,  and measuring the reactions across the scenarios against an intended reaction.

 One application of A?B Testing is to test two application versions at the same time. By splitting the traffic 50/50 between two versions of an application or website, you are able to determine which version is more popular, faster, a better fit, etc. … whichever criteria you have determined are most important.

For example, a website might experiment with a different layout. While unit testing, integration testing, and user acceptance testing may be successful, determining if the layout is more popular or results in more leads/orders/profits/etc. is done by A/B testing with the previous layout. In this scenario it is common to randomly split web traffic between the two layouts.

In a microservices context, A/B testing directs traffic randomly between the two versions and logs, traces and monitoring are used to determine which is better.

If you are using Red Hat OpenShift, one tactic for A/B Testing is to spin up an equal number of pods for the two versions of your application and then establish one route that uses a round robin load balancer to direct traffic to the pods.

Using Istio to implement A/B Testing gives you more control over the traffic. This is the suggested method of A/B Testing against OpenShift applications.
