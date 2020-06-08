# LXC - Container

![Linux_Containers_logo](https://user-images.githubusercontent.com/42691369/83990953-ead8ef80-a968-11ea-8467-ca31c773edd3.png)

LXC (Linux Containers) is an operating-system-level virtualization method for running multiple isolated Linux systems (containers) on a control host using a single Linux kernel.

The Linux kernel provides the cgroups functionality that allows limitation and prioritization of resources (CPU, memory, block I/O, network, etc.) without the need for starting any virtual machines, and also namespace isolation functionality that allows complete isolation of an application's view of the operating environment, including process trees, networking, user IDs and mounted file systems.

LXC combines the kernel's cgroups and support for isolated namespaces to provide an isolated environment for applications. Early versions of Docker used LXC as the container execution driver, though LXC was made optional in v0.9 and support was dropped in Docker v1.10.


Overview :

         LXC provides operating system-level virtualization through a virtual environment that has its own process and
         network space, instead of creating a full-fledged virtual machine. LXC relies on the Linux kernel cgroups
         functionality that was released in version 2.6.24. It also relies on other kinds of namespace isolation  
         functionality, which were developed and integrated into the mainline Linux kernel.
         
Security :

         Originally, LXC containers were not as secure as other OS-level virtualization methods such as OpenVZ in Linux 
         kernels before 3.8, the root user of the guest system could run arbitrary code on the host system with root 
         privileges, much like chroot jails. Starting with the LXC 1.0 release, it is possible to run containers as regular 
         users on the host using "unprivileged containers". Unprivileged containers are more limited in that they cannot 
         access hardware directly. However, even privileged containers should provide adequate isolation in the LXC 1.0 
         security model,if properly configured.
         
Alternatives :

         LXC is similar to other OS-level virtualization technologies on Linux such as OpenVZ and Linux-VServer, as well  
         as those on other operating systems such as FreeBSD jails, AIX Workload Partitions and Solaris Containers. In 
         contrast to OpenVZ, LXC works in the vanilla Linux kernel requiring no additional patches to be applied to the 
         kernel sources. Version 1 of LXC, which was released on 20 February 2014, is a long-term supported version and i
         ntended to be supported for five years.[7]
