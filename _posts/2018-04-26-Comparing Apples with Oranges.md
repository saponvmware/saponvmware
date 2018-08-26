---
title: Comparing Apples with Oranges
excerpt: "Is comparing physical to virtual valid"
header:
  teaser: ""
category:
tags: [SAP, VMware, Performance, vSphere]
---

![Apples vs Oranges]({{ site.url }}/images/appleorange.jpg)

*Disclaimer: Picture by sap.com*

**Physical vs Virtual testing guidelines**
Very often we are having discussions about the comparison of physical vs virtual installation of SAP systems. These discussions are mostly driven by the goal of comparing apples with apples but if you have a more detailed look into the details you will figure out that the discussions end up actually comparing apples with oranges. The goal of this blog article is to give you another view on this topic.

**Cores vs vCPUs**
If you compare the physical vs virtual CPU (vCPU) you have to consider Cores vs Threads vs vCPU. A vCPU is also known as Hardware Execution Context (HEC) and represents a physical thread. Current Intel CPUs provide Hyper Threading – doesn’t doubles your performance. So, if you compare Cores vs vCPU (one to one) please keep in mind that the physical core will be able to use the benefit of Hyper Threading. Comparing apples with apples in this context means to benchmark cores without Hyper Threading vs vCPUs.

**NUMA vs vNUMA**
VMware vSphere is using a mechanism to provide the NUMA architecture to the virtual machine and is enabled for virtual machines with more than 8 vCPUs by default. This technology is called vNUMA. Ensure that you’re providing the operating system inside the virtual machine with the same vNUMA architecture as your physical hardware. Please be aware that NetWeaver itself is not NUMA aware (SAP basis administrators can use commands like NUMACTL), but vSphere tries to schedule the threads NUMA optimized.

**Storage IO**
The storage layout could also impact the result of a physical to virtual benchmark. Verify that you are using the same storage type and storage protocol in both installations. Keep in mind that in a virtual environment you are using VMDK on VMFS data stores. Distribute the database files in the same ways as in the physical world. Use the latest VMware Tools and the current driver for the virtualized SCSI controller.

**Network IO**
If you are running a distributed system network latency could warp the test results. Ensure you use the latest driver for the virtual network card and you have applied the best practice about low latency in a vSphere environment. This means to reduce or disable IRQ coalescing on the virtual machine and hypervisor level. In the same hardware scenarios IRQ coalescing is not a parameter of the physical network card on the hypervisor but a parameter in the management of the hardware. Ensure you are using the current version of the VMware Tools and the latest driver for the virtualized network adapter.

**Operating System Installation**
If you compare a physical vs virtual installation, ensure you have installed the same operating system with the same patch level. In a physical installation you will benefit from native and hardware optimised drivers from the hardware vendor. So, ensure you have installed the latest VMware Tools for the correct operating system. The VMware Tools provide the optimised drivers for the virtual hardware.

**Noisy Neighbours**
Comparing apple with apples ensure that in the virtual environment there is no noisy neighbour. This means that no other workload like other virtual machines are running on the same host and producing noise. This has a direct impact on the benchmark. On a physical server, you will also be running only one installation.

**Distributed vs Central Installation**
We saw that customers are benchmarking distributed installation vs central installations, which has an impact on the latency. With a distributed installation, you install the database, central services and application server(s) on different operating systems. With a central installation you’re running all components on the same operating system. On a central installation the communication between the application server and database server has a lower latency. Keep in mind, that with a lower latency between database and central services & application server you will benefit.

**Conclusion**
If you are in the situation where you need to compare a physical to virtual installation, always try and compare apples with apples in all cases if possible. After you get your results, validate the results by confirming that the virtualization overhead is valid. In case the numbers are unrealistic review all components to make sure you are not comparing apples with oranges.

*Tags: SAP, VMware, Performance, vSphere*
