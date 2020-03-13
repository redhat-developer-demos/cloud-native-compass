# Batch Size

In the DevOps world, batch size is the amount of changes accumulated between each one of your software releases and/or deployments into production. It’s directly connected to two other very import metrics: lead time, and cycle time.

Some practitioners consider batch size to be the most relevant metric in any DevOps strategy: it’s easily measured no matter how mature (or immature) is your organization, and it has a direct correlation with risk mitigation.

First, let’s discuss the correlation with risk mitigation. Updating software into production is risky: usually software releases bring new bugs, and bugs might impact your business results. But not updating software is also risky: existing bugs or security issues won’t get fixed without a new software release, and not providing capabilities to your software fast enough to keep it up to the business requirements pace is also very dangerous for your long term wealthy.

Changes in a software deployment pipeline encompasses three different scopes: code, environment, and data. Bugs into production environments are almost always associated with changes in one of these scopes. That’s the reason why reducing batch size is one of the primary goals of any DevOps strategy: the larger the batch size, the larger the risks associated to having bugs into production.
