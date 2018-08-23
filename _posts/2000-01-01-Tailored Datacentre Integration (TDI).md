---
title: Tailored Datacentre Integration (TDI)
excerpt: "TDI vs Appliance Model"
header:
  teaser: ""
category:
tags: [SAP, SAP HANA, TDI, VMware, vSphere]
---

SAP HANA is SAP’s flagship in-memory database and its absolute focused database for critical SAP applications, and therefore almost all new SAP applications are designed for SAP HANA.

To guarantee a certain kind of performance, SAP introduced the appliance model for SAP HANA.   
This appliance models are designed, configured and supported by the different server vendors. The appliance model consists normally of the server, the storage and the top-of-rack switch and in cases of virtualization with vSphere as hypervisor.

This appliance model has pros and cons about the flexibility. Here is an example: Think of a scenario with the server from your preferred server vendor including the storage from your preferred storage vendor and so on. Now, what is the scenario if the customer has already an SAP HANA certified storage system?

For this kind of customer requests, SAP defined the SAP HANA Tailored Datacentre Integration (TDI) model. This model is created to give customers more “freedom” to use existing environment components. But how to ensure the “promised” performance in a non-Appliance approach?

In a TDI model, the customers need to look after the performance of IOPS. To help the customer, SAP provides a tool called “HWCCT” to benchmark the IOPS performance of the infrastructure landscape. This tool should also be used in a virtualized environment. Particularly in production environment. In a virtualized Multi-VM environment in production the customer needs to run the tools at the same time in each of the virtual machines on the same physical server.

In a nutshell, the customer also needs to run the “HWCCT” in a virtualized SAP HANA in production to determine if the storage subsystem is able to meet the SAP HANA KPIs.

Conclusion: Thinking the TDI model is the right approach in the SAP on VMware matter and the experience shows that most customers are using the TDI model in a vSphere environment.

For more details about the “HWCCT”, please see the relevant SAP Note.

* 1943937 - Hardware Configuration Check Tool - Central Note.
(SAP user required)

*Tags: SAP, SAP HANA, TDI, VMware, vSphere*
