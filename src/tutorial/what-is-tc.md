---
title: What is TaskCluster?
followup:
  links:
    hello-world: Create a task to see TaskCluster in action!
---

*TaskCluster* is a set of components that manages task queuing, scheduling,
execution and provisioning of resources. It was designed to run automated
builds and tests at Mozilla.

Like most software organizations, Mozilla needs to compile and test the code its developers produce.
The scale of this work is staggering: many days of computer time are required for every change, and developers make changes many times per day, every day.
TaskCluster supports execution of all of those build and test jobs quickly (so developers get the information they need) and efficiently (so we do not waste our precious resources).
To support the rapid pace of change, TaskCluster is self-serve: you can accomplish just about anything you need to yourself, when you need it.
And the service is a Mozilla product: open and transparent, secure and reliable.

The "TaskCluster platform" supports the execution of tasks: the fundamental purpose of TaskCluster.
But it is the "core services" which make TaskCluster useful.
These provide the tools and integrations necessary to support our complex build, test, and release processes.
These include

 * Integrations with version-control systems like Mercurial and Git, to start tasks when developers commit code
 * Indexes of completed tasks, to find the results of build and test runs
 * Hooks to schedule tasks at specific times (e.g., a nightly build)
 * Secure storage for secret data such as API keys required to complete tasks
 * Workers of various types that will actually run the tasks.

---

## Is it Mozilla-specific?

In principle, no, TaskCluster could be useful to any organization with needs similar to Mozilla's.
While we have built some Mozilla-specific integrations, the platform and many of the core services could be re-used without change in another organization.

However, the platform is not presently designed to be easily redeployed.
While it is by no means impossible to set up a second instance of TaskCluster outside of Mozilla, neither is it a turnkey installation.
We hope to address this soon, once we have demonstrated the usefulness of the platform.
