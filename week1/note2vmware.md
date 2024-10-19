# Download Vmware
- VMware Workstation: 
A desktop virtualization product that allows users to run multiple operating systems on a single PC.

# Virtualization:
- Is the process of creating the software based or virtual, version of something whether that is compute, storage, networking, servers or applications.Hypervisor makes virtualization feasible

    # Hypervisor:
    - Piece of software that runs above physical server or host.
    - There are different types of them, essentially pull the resources from the physical server and allocate to virtual environment.
    - 2 main types: 1. Type 1 and 2. Type 2
        # Type 1 (Baremetal) [One tht's in college]
        - It is installed directly on top of physical server, also called BARE METAL.
        - Frequently used, secure, low latency(minimal delay b/w input and corresponding output). Vmware ESXI, Microsoft Hyper-V etc
        # Type 2 (Hosted) [One I'm using]
        - There is a layer of host os between physical server and hypervisor , also called hosted
        - Less used, for end user virtualization
        - Oracle, virtual Box or Vmware workstation
        - High latency

    - After having the hypervisor installed, you can build virtual environment or machines simply put vms
    - Vm is software-based computer
    - Run like physical computer have os and applications and completely independent of each other, many can be run
    - Hypervisor manages the resources from physical server
    - Since independent we can run diff os on diff vms on the hypervisor
    - They are also portable, u can move vm from one hypervisior to another hypervisor on completely different machine almost instantaneously.

    # Benefits of Virtualization
    - Less Cost 
    - Agility + speed : it is more simple and quick rather than learning the new environment.
    - Lower downtime:If one hosts goes dwon unexpectedly we can move one vm to another hypervisior on different physical server, then we can simply move our vm very quickly.