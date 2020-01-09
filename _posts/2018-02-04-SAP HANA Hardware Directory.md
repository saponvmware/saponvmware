---
title: SAP HANA Hardware Directory
excerpt: "Find Certified SAP HANA servers for Virtualization on vSphere"
header:
  teaser: ""
category:
tags: [SAP, VMware, SAP HANA]
---

<<<<<<< HEAD
As many SAP practitioners know, if you want to run a supported SAP HANA server configuration you will need  a server listed in SAP HANA Certified Hardware Directory.
=======
If you want to run a supported SAP HANA server configuration you need to ensure the is server listed at the SAP HANA Certified Hardware Directory.
>>>>>>> 5162b2d2e79d2a87a5a3d9c18d453bb1e6d7f557
This directory is available at:

[SAP HANA Hardware Directory](https://www.sap.com/dmc/exp/2014-09-02-hana-hardware/enEN/appliances.html)

![SAP HANA Hardware Directory]({{ site.url }}/images/sap-hana-hardware-directory.jpg)
*Disclaimer: Picture by sap.com*

<<<<<<< HEAD
If you want to virtualize your SAP HANA system, you should verify that the server is also listed at VMware HCL. Not all servers at SAP’s hardware directory is on VMware’s HCL. Additionally, not all server CPU (Haswell, Broadwell) and not all server CPU counts (4-way vs 8-way) are certified by SAP for SAP HANA virtualization with VMware vSphere.
=======
If you want to virtualize your SAP HANA system, you should verify that the server is also listed at VMware HCL. Not all servers at SAP’s hardware directory is on VMware’s HCL. Additionally, not all server CPU (Haswell, Broadwell) and not all server CPU counts  (4-way vs 8-way) are certified by SAP for SAP HANA virtualization with VMware vSphere.
>>>>>>> 5162b2d2e79d2a87a5a3d9c18d453bb1e6d7f557

Here is a quick list to help you to select a server for virtual SAP HANA which is supported by SAP and VMware.

<<<<<<< HEAD
**Check if your server is listed on SAP’s Hardware Directory**:  
Verify your preferred server is listed at SAP’ Hardware Server Directory, not all servers are certified by SAP for productive SAP HANA workloads.
=======
**Check if your server is listed on SAP’ Hardware Directory**:  
Verify the preferred server is listed at SAP’ Hardware Server Directory, not all servers are certified by SAP for productive SAP HANA workloads.
>>>>>>> 5162b2d2e79d2a87a5a3d9c18d453bb1e6d7f557

**Check the deployment type for the preferred server**:  
SAP HANA has different deployment options - scale-up vs scale-out - plus the application type like Business Suite on HANA (BSoH), Business Warehouse on HANA (BWoH), Datamart (DM) and S/4 HANA.

**Check that the sever is on VMware’s HCL**:    
<<<<<<< HEAD
Not all servers at SAP’s Certified Hardware Directory are certified and supported on vSphere. In this case verify that your selected server is on the HCL of VMware.  
=======
Not all servers at SAP’s Certified Hardware Directory are certified and supported by VMware vSphere. In this case verify that your selected server(s) are on VMware's HCL.

>>>>>>> 5162b2d2e79d2a87a5a3d9c18d453bb1e6d7f557
[VMware Compatibility Guide at vmware.com](https://www.vmware.com/resources/compatibility/search.php)

**Check if CPU type & CPU count is supported by SAP HANA on VMware**:  
There are limitations on the CPU Type (like Haswell, Broadwell) and CPU count (2, 4, 6 or 8-way servers).

[SAP HANA on VMware vSphere at scn.sap.com](https://wiki.scn.sap.com/wiki/display/VIRTUALIZATION/SAP+HANA+on+VMware+vSphere)

**Check additional features like hardware partitioning**:  
Some server has additional features like hardware partitioning (e.g. Fujitsu, Hitachi) for these additional features please check the SAP Marketplace Knowledge Base.

[SAP Notes at sap.com](https://launchpad.support.sap.com/#/solutions/notes/?q=) (SAP user required)

In addition to the above checks as always work with your preferred server vendor, SAP and VMware.

*Tags: SAP, VMware, SAP HANA*
