---
title: Benefits of virtualization of SAP 
excerpt: "What are the benefits of running SAP on VMware"
header:
  teaser: ""
category: [Blog]
tags: [SAP, VMware, SAP HANA]
---

I was asked more than one time what the befits of running SAP and SAP HANA in a virtualized environment are. And the most valid arguments are High Availability, Lower Total Cost of Ownership, Faster Time to Value, and Security and Compliance.

![BLOG]({{ site.url }}/images/sapvmware.jpg)
*Disclaimer: Picture by vmware.com*

*	High Availability
With VMware vSphere High Availability (HA) you can get an availability of 99.9%. The uptime is maximized as failover is automated. For example, a VM will fail over, if the vSphere ESXi hosts the VM was running on, is not available anymore, or the virtual machine stops responding. No data loss will be lost, and downtime will be minimized when vSphere HA restarts the VM on a different Host. Live migrating workload from one host to another, can furthermore reduce the downtime during planned activities.

* Lower Total Cost of Ownership
VMware’s Software Defined Datacenter (SDDC) provides the opportunity to automated data center operations, as any component of the SDDC is software based and providing an API. This ensures the possibilities of “end-to-end” automation processes of the SDDC stack including compute, storage and network. With the automated infrastructure delivery and provisioning of applications like SAP HANA, the Total Cost of Ownership will be reduced.

* Faster Time to Value
With the Software Defined Datacenter (SDDC) the deployment in hours is possible instead of days with rapid and automated provisioning. This ensures scalability and consistency deployment across environments thought pre-defined blueprints and anything as a Service like XaaS. In the SAP and SAP HANA context, VMware is offering an adapter for SAP Landscape Management based on VMware Orchestrator to “bridge” the SAP landscape and VMware environment.  

* Security and Compliance
VMware NSX is VMware’s Software Defined Network (SDN) solution. This allows to protect the network on the hypervisor level and ensure the security hardening. NSX allows to create security groups, cluster the SAP workload and enforce data protection and privacy. A use case is, to ensure the network separation of systems after system copy or system clone, that the data consistency of an SAP landscape guarantee.

*Tags: SAP, SAP HANA, VMware*
