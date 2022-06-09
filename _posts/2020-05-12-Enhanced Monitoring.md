---
title: Enhanced Monitoring
excerpt: "Enable Enhanced SAP System Monitoring"
header:
  teaser: ""
category: [Blog]
tags: [VMware, vSphere, Monitoring]
---

For the operation a virtualized SAP system on Windows, Linux or Cloud environment SAP requires the setup of the enhanced SAP system monitoring. The reason for this requirement is, that in physical environments all recourses are assigned to the operating system. In a virtualized environment the underlaying resources are shared of one or more virtualized operating systems.

In resources constrained situations the SAP basis administrator benefits of the important information about the underlaying physical resources available to the different virtualized systems. Therefore, the setup of the enhanced SAP monitoring is mandatory by SAP of virtualized Windows and Linux systems, this is also required for SAP systems in a cloud environment.

After the setup of the enhanced SAP system monitoring read access on performance metrics and specified configuration of the hypervisor and virtual machines are provided in the SAP system itself or in the SAP Solution Manager. This information is essential for the SAP support and for performance analysis of the virtualized SAP systems. The metrics are displayed in the ABAP transaction(s) ST06, OS07 or OS07N, depends on the NetWeaver release, of each configured SAP system.

![Space Center]({{ site.url }}/images/spacecenter.jpg)
*Disclaimer: Picture by pixabay.com*

The prerequisite of an SAP system is the SAP Host Agent - in the past the SAPOSCOL service was used for the enhanced monitoring - therefore check and update the version of the “SAP Host Agent”. The minimum SAP Host Agent required version of the SAP release is 7.21. For vSphere as Hypervisor patch level required version 05 - for Windows Server 2016 as guest operating system patch level version 24. Check the version by execute the operating commando *saphostexec -version*. Besides the requirement of the SAP Host Agent, the VMware Tools needs to be installed.

To provide the full set of virtualization data, two advance parameters on the virtualization host and virtual machine needs to be configured.

Enable *Misc.GuestLibAllowHostInfo = "1"* on the host to provide the hypervisor data to the virtual machine.

Enable *tools.guestlib.enableHostInfo = "TRUE"* on the virtual machine to receive hypervisor data from virtualization host.

With the commands *saposcol.exe -d* on Windows and with */usr/sap/hostctrl/exe/saposcol -d* on Linux on the specific virtual machine, you could get also the virtualization data.

For more information please refer to the following SAP Notes:

[SAP Note: 1606643 - Linux: VMware vSphere host monitoring interface](https://launchpad.support.sap.com/#/notes/1606643)

[SAP Note: 1409604 - Virtualization on Windows: Enhanced monitoring](https://launchpad.support.sap.com/#/notes/1409604)

*Tags: VMware, vSphere, Monitoring*
