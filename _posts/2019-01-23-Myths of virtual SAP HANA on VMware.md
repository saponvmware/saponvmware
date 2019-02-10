---
title: Myths of virtual SAP HANA on VMware
excerpt: Demystifying virtual SAP HANA myths
header:
  teaser: ""
category:
tags: [SAP, SAP HANA, VMware]
---

There are some myths in the field about the virtualization of SAP HANA on VMware. This blog article shows the most named myths and their truths.

![Any Questions]({{ site.url }}/images/anyquestions.jpg)  
*Disclaimer: Picture by pixabay.com*

**Myth**: Limited memory size of SAP HANA on vSphere, the largest implementation is 1 TB of virtual memory.  
**Truth**: The supported limitation of virtual machine memory size is 6 TB on OLTP workload and 3TB on OLAP workload – both on Intel Skylake CPUs. “The maximum size for Skylake of a virtual SAP HANA instance is limited CPU-wise by the maximum size of a virtual machine on VMware vSphere 6.5 and 6.7 release, which is 128 vCPUs on 4 Sockets (4 sockets on up to 8 socket hardware), and 6TB of RAM. Due to the underlying certified hardware OLAP can only use with maximum 3TB, the actual usable RAM is a matter of SAP Sizing.”
SAP Note [2393917](https://launchpad.support.sap.com/#/notes/239317) - SAP HANA on VMware vSphere 6.5 and 6.7 in production

**Myth**: Other applications are not supported on the same hosts besides SAP HANA virtual machines.  
**Truth**: Co-deployments besides SAP HANA virtual machines in production is supported independent of SAP HANA or Non-SAP HANA virtual machines on the same vSphere host. “SAP HANA VMs can get co-deployed with SAP non-production HANA or any other workload VMs, as long as the production SAP HANA VMs are not negatively impacted by the co-deployed VMs. …”
SAP Note [2393917](https://launchpad.support.sap.com/#/notes/239317) - SAP HANA on VMware vSphere 6.5 and 6.7 in production.

**Myth**: On technical or engineering related challenges with virtualized SAP HANA you’re on your own.  
**Truth**: Both, SAP and VMware have a long strategic partnership and together both companies are providing a joined support for virtualized SAP HANA on VMware.
“SAP and VMware will assist joint customers in collaborative support services and problem resolution, backed by a global technology partnership agreement and dedicated support staffing.”
[VMware Announces Support from SAP of VMware ESX Server for Production Environments](https://ir.vmware.com/overview/press-releases/press-release-details/2007/VMware-Announces-Support-from-SAP-of-VMware-ESX-Server-for-Production-Environments/default.aspx)

**Myth**: The virtualization overhead degrades the performance severely.  
**Truth**: There is a performance overhead by the hypervisor. But, in the past “physical to virtual” benchmarks showed an overhead of less than 10% compared to bare metal servers. More details of a “BWL-EML” benchmarks are documented (Page 6) by HPE with a delta of 5%.
[Virtualized SAP HANA performance evolution with the HPE ConvergedSystem 500 and VMware vSphere 6.0](https://h20195.www2.hpe.com/v2/getdocument.aspx?docname=4aa6-6194enw)

**Myth**: The SAP HANA data is not accurately and/or properly stored on a virtual environment and could be causing functional errors.  
**Truth**: After two years of intense testing, not a single functional error occurred while running SAP HANA on VMware platform based on vSphere hypervisor.

**Myth**: Disaster Recovery (DR) is not possible and not supported for virtualized SAP HANA workload.  
**Truth**: Disaster a Recovery is supported by different technologies and products. In the case of VMware products and technologies VMware vCenter Site Recovery Manager (SRM) is supported for SAP HANA workload on VMware vSphere.

**Myth**: VMware’s technology vSphere vMotion for the live migration is incompatible with SAP HANA workload.  
**Truth**: VMware vSphere vMotion can be used successfully to migrated running virtual machines in a SAP HANA environment when the best practices are followed.
[Architecture Guidelines and Best Practices for Deployments of SAP HANA on VMware vSphere Guide](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/pdf/whitepaper/sap_hana_on_vmware_vsphere_best_practices_guide-white-paper.pdf)

**Myth**: Customers can ignore the recommendations of the SAP HANA on VMware best practices guide.  
**Truth**: SAP and VMware invested considerable resources to create best practices for SAP HANA workload on VMware vSphere to reduce the complexity and to archive the optimal support results.

**Myth**: VMware can’t be scaled-out for SAP HANA workload on vSphere hypervisors.  
**Truth**: SAP HANA Scale-out is officially and fully supported by SAP and VMware since SAP HANA 1.0 SPS 09. With this support it is possible to scale-out SAP HANA until 16 nodes and up to 64 TB of memory for BW on HANA workload.
SAP Note [2393917](https://launchpad.support.sap.com/#/notes/2393917) - SAP HANA on VMware vSphere 6.5 and 6.7 in production

**Myth**: Virtualizing of SAP HANA requires a fundamental change in the operation and additional resources needed.  
**Truth**: In the properly designed environment with appropriate supporting dependencies and assets, SAP HANA virtual machines are simply another application running on the vSphere hypervisor, achieving also the goals of lower TCO, better service levels and faster time-to-value.

*Tags: SAP, SAP HANA, VMware*
