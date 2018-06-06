# Learning what Linux is

## Understanding What Linux is

Linux is a computer OS. An OS consists of the software that manages your computer and run application on it.

OS's essential features:

- Detecting and preparing hardware.
- Managing processes.
- Managing memory.
- Providing user interface.
- Controlling filesystems.
- Providing access and authentication.
- Offering administrative utilities.
- Starting up services.
- Programming tools.

Advanced features in Linux:

- Clustering.
- Virtualization - To manage resources effectivel, Linux can run as virtual host. On that host, you can run other Linux systems, Microsoft Windows, BSD, or other OS as virtual guests. To outside world, each of those virtual guest appears as a seperate computer. KVM and Xen are two technologies in Linux for creating virtual hosts.
- Clound Computing - To manage large-scale virtualization enviroments, you can use full-blown cloud computing flatforms based on Linux. (Projects: OpenStack and Red Hat Enterprise Virtualization)
- Real-time computing - Linux can be configured for real-time computing, where high-priority process can expect fast, predictable attention.
- Specicalized Storage - Instead of just storing data on the computer's hard disk, many specicalized local and networked storage interfaces are available in Linux. (Shared storage devices: iSCSI, Fibre Channel and Infiniband). (Open souce flatforms as projects: Ceph, GlusterFS)

## Understanding How Linux Differs from other OSs

On Other OSs:

- You cannot see the code used to create the OS
- You, therefore, cannot change the OS at its most basic levels if it doesn't suite your needs - and you cannot use the OS to build your own OS from source code.
- You cannot check code to find bugs, explore security vulberabilities, or simply learn what that code is doing.
- You may not able to plug your own software to the OS if the creator of the OS don't want to expose the programming interface to outside the world.