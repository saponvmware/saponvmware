---
title: SAP Classic Best Practices
excerpt: "TOP 10 Best Practices for SAP Classic"
header:
  teaser: ""
category:
tags: [SAP, vSphere, VMware, SAP Classic, Best Practices]
---

This article describes the “Top 10” Best Practices to run “SAP Classic” workload on VMware vSphere. Please keep in mind, this article covers “SAP Classic” like SAP NetWeaver and not SAP HANA.

* Use the latest processor generations, especially with Intel VT-x and AMD AMD-V technology to get the best benefits from technology like EPT and VT-d from Intel and AMD-V and AMD-V from AMD. This includes also the BIOS setting to maximize the performance of the server.

* Do not overcommit virtual memory and therefore set the memory reservation to the same size of the configured size of the virtual machine memory. This best practice is highly recommended for production SAP workload (PRD) and could also be used for quality assurance (QAS) and development systems (DEV).

* Enable hyper threading (HT) minimum for the SAP application server, as the SAP dialog multiplexing are benefiting of hyper threaded CPUs. If your SAP landscape are executing more single thread batch jobs, it could make sense to disable hyper threading.

* Ensure that vNUMA is used – if enabled hot add CPU, vNUMA is disabled by default – to represent the underlying physical NUMA architecture. The vSphere Host will typically configure vNUMA to match the NUMA architecture of the host.

* Configure all vSphere hosts and virtual machines operating guest systems to use the same NTP-Server (Network Time Protocol).

* Install the latest VMware Tools or Open VMware Tools benefit of paravirtualized devices like the storage controller “pvscsi” and the network adapter “vmxnet3”. Also, the SAP aware monitoring inside SAP itself needs the installation of the VMware Tools.

* Use the paravirtualized storage controller “pvscsi” to get the most performance of the I/O in a virtualized environment. Also ensure that the virtual disks are distributed over all of the four available adapters.

* Configure the paravirtualized network adapter “vmxnet3” to get the height throughput with the lowest latency. This optimized adapter could pass the traffic between virtual switches and the physical network with minimal overhead.

* You could overcommit virtual CPU (vCPU) and it is supported by SAP itself but configure the vCPU only in a reasonable manner. Overcommitting is possible, as the virtual machine workload might not peak at the same time.

* Configure the “Enhanced Monitoring” for virtual environments to provide the performance related date to the SAP system, collected by the “SAP CIM Provider”.

More details could be found on more than 60 pages at the SAP on [VMware Best Practices Guide](https://www.sap.com/dmc/exp/2014-09-02-hana-hardware/enEN/appliances.html)

![SAP on VMware Best Practices]({{ site.url }}/images/bestpractices.jpg)
*Disclaimer: Picture by vmware.com*

List of the most important SAP Notes for the virtualization of SAP on VMware.

* SAP Note 1492000 - General Support Statement for Virtual Environments
* SAP Note 1122387 - Linux: SAP Support in virtualized environments
* SAP Note 1409608 - Virtualization on Windows
(SAP user required)

*Tags: SAP, VMware, vSphere, SAP Classic, Best Practice*
