---
title: SAP on VMware Health Check
excerpt: "What should be considered during an SAP Health Check?"
header:
  teaser: ""
category: [Blog]
tags: [SAP, SAP HANA, VMware, Architecture]
---

Health Checks are not unusual in a VMware vSphere environment, but what need to cover in addition for a SAP on VMware Health Check?

Typically, a Health Check reviews and analyzes the current architecture design in conjunction of VMware’s Best Practices and recommendations. In addition to this best practices and recommendation SAP and VMware defined an additional set of recommendation and requirement for the support of SAP and SAP (HANA) on VMware. Those documented in a related SAP Notes (SAP user required) and in the Best Practice documents provided by VMware.

**Typical process approach:**
* Gathering information
* Evaluating and validating
* Documenting and remediating

Information sources:

**Sizing**
* SAP Quick Sizer
* Hardware Vendor
* Compute, Storage and Network
* VMware ESXi nodes
* HA and DR architecture

**SAP Landscape and Design**
*	Type of SAP system/application
* SAP Landscape architecture  
* 2-tier or 3-tier implementation
* Compute, Storage and Network requirements
* High Availability and Disaster Recovery requirements
* Production and non-production deployments
* On-Premise, Off-Premise or Hybrid requirements

**Virtual Machine**
* VMware Tools versions
* Best Practices for ‘SAP on VMware’ workload
* SAP based configuration
* OS-vendor recommendations

**Storage Layout and Design**
*	Type of Storage
*	Storage architecture
*	Storage layout
*	I/O Capacity
*	Storage-vendor recommendations

**Network Layout and Design**
*	Network Bandwidth
*	Network Adapter
*	Network Architecture
*	Network Redundancy
*	Network-vendor recommendation

**Cluster and Resource Design**
* Design of vSphere Clusters
* Configuration of Resource Pools
* Provisioning
* Over Commitment

**Disaster Recovery Design**
* Disaster Recovery architecture
* RPO and RTO requirements

**Disclaimer:** The list above has no claim to completeness.

The finding of an SAP on VMware Health Check should be documented by the scope of the assessment, the covered systems and the related vSphere infrastructure. The output helps to identify gaps how well the infrastructure is designed and configured. This identifies the need of attentions nor remediation about the SAP on VMware Best Practices and recommendations of both vendors - SAP and VMware.

*Tags: Architecture, SAP, SAP HANA, VMware*
