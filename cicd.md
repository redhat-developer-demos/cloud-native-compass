# CI/CD

Acronym for Continuous Integration/Continuous Delivery or Continuous Integration/Continuous Deployment.

Continuous Integration (CI) is the practice of merging all developer software branches (or changes) into the master copy (or “trunk”) several times a day. The theory behind CI is that, at any time, a build successful build should be possible from the master trunk of the software. Part of the build process includes automated unit testing. To avoid partial features from being included, Feature Toggles can be used to ignore unfinished sections.

Automating the process is done by using a build server, which runs after every software commit. This gives a constant update on the status of the software.

Continuous Delivery extends CI by assuring that the successfully-built code is ready for rapid deployment. Continuous Delivery is not the practice of putting software into production; rather, it is making the software available for production use. The decision to deploy the software can be automatic (Continuous Deployment) or manual.

Continuous Delivery is the goal to be reached in order to be successfully embracing DevOps.

Continuous Deployment differs from Continuous Delivery. It is the practice of deploying software to production automatically after a successful build. For most, this is either impractical, too risky, or violates regulations. Manually deploying software is often the preferred method of deployment; Continuous Deployment is best for low-risk software or highly-performant development teams.
