---
title: VMware Support at SAP
excerpt: "Discription of the SAP VMware Alliance Support"
header:
  teaser: ""
category:
tags: [SAP, VMware, Support]
---

Often we receive questions from  customers requiring support from either VMware and/or SAP to resolve performance or functional issues. If you know the issue is caused by a VMware product or feature open a ticket with  the VMware Global Support and Services (GSS) organization and if the issue is related to a SAP product open a ticket with the SAP Support organization.

What  if its not clear where the cause of the problem is, VMware or the SAP layer? In this case you could open a ticket with SAP first. SAP will investigate the issue and if they conclude it is not SAP related,  SAP will assign the ticket to another queue in their support system. There are separate queues/components based on the database type (SAP HANA, Sybase, MaxDB, etc), the operation system vendor and the hypervisor vendor like VMware.

As a SAP certified hypervisor vendor VMware has two support components inside of SAP’s support system. The two components are: **BC-OP-NT-ESX** for virtualized SAP on Linux and **BC-OP-LNX-ESX** for virtualized SAP on Windows. Now there is an additional support component monitored by VMware for the SAP Landscape Adapter (VLA) for LVM (Landscape Virtualization Manager) and LaMa (Landscape Manager) - BC-VCM-LVM-VMW.

![BC-OP-$-ESX]({{ site.url }}/images/bc-op-*-esx.jpg)

VMware has support engineers in their Global Support & Service (GSS) organization  who have both VMware and SAP expertise that have access to SAP’s support system who also monitor the support requests created in the SAP support system and can pro-actively take the ownership of support tickets if applicable to VMware.

**Conclusion:** For production support issues If you have identified the level, VMware or SAP where the issue is occurring, then open a support request with the corresponding vendor. In all other cases you can open a support ticket with SAP’s support organization who will take care of the process and if required will assign the ticket to a VMware support component.

*Tags: SAP, VMware, Support*
