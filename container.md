# Container

Linux containers are technologies that allow you to package and isolate applications with their entire runtime environment — all of the files necessary to run; operating system, data, binaries, dependencies, etc. This makes it easy to move the contained application between environments (development, test, production, etc.) while retaining full functionality.

To put a finer point on it, imagine you’re developing an application. You do your work on a laptop and your environment has a specific configuration. Other developers may have slightly different configurations. The application you’re developing relies on that configuration and is dependent on specific files. Meanwhile, your business has test and production environments which are standardized with their own configurations and their own sets of supporting files. You want to emulate those environments as much as possible locally, but without all of the overhead of re-creating the server environments. So, how do you make your app work across these environments, pass quality assurance, and get your app deployed without massive headaches, rewriting, and break-fixing? The answer: Containers. The container that holds your application has the necessary configurations (and files) so that you can move it from development, to test, to production without all of the nasty side effects. Crisis averted–everyone’s happy.

## Isn’t this just virtualization?

Yes and no. Here’s an easy way to think about the two:
* Virtualization lets many operating systems run simultaneously on a single system.
* Containers share the same operating system kernel and isolate the application processes from the rest of the system.

![/images/containers.png](/images/containers.png)  

What does this mean? For starters, having multiple operating systems running on a hypervisor, the software that makes virtualization work, isn’t as lightweight as using containers. When you have finite resources with finite capabilities, you need lightweight apps that can be densely deployed. Linux containers run from that single Linux kernel, sharing it across all of your containers, so your apps and services stay lightweight and run swiftly in parallel.

Because containers are self-contained they can be started quickly, typically in under one second. This makes containers ideal for auto-scaling environments such as Kubernetes and OpenShift.
