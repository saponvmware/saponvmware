---
title: Scale-up vs Scale-out
excerpt: "What is the difference between SAP HANA Scale-up and Scale-out"
header:
  teaser: ""
category: [Blog]
tags: [SAP, SAP HANA, VMware, Scale-up, Scale-out]
---

During the deployment of SAP HANA databases, SAP offers at least two options how the SAP HANA landscape architecture looks like - Scale-up and Scale-out. The two deployment options could also describe as vertically (scale-up) and horizontally (scale-out).

**Scale-up:**

In a scale-up architecture, the SAP HANA database is running on a single server and this server could have many resources as possible. The Scale-up option also called by SAP as “Single Host SAP HANA Configuration”.
The limit is by the server vendors, CPU & Memory architecture and SAP HANA hardware certification. Typical application for scale-up are Suite on HANA (SoH) or S/4 HANA.

**Scale-out:**

In a scale-out architecture, the SAP HANA database is “partitioned” over different servers. This cluster of SAP HANA systems represent the SAP HANA database itself. In a scale-out architecture, the data is distributed over the different nodes of the SAP HANA system. A scale-out environment requires a “inter-node network” for the communication between the different nodes.

![Scale-up vs Scale-out]({{ site.url }}/images/scale-up-vs-scaleout.jpg)
*Disclaimer: Picture by saphana.com*

**Go scale-up or scale out?**

From this point of view - go scale-up, as long you could go scale-up - may this advice might change in future.
The deployment type of scale-up has same benefits against scale-out. The performance is invariable better as access of local memory is always faster as memory access across network. The Total Cost of Ownership (TCO) could be lower as the “simplified” single deployment of server, storage and network including connectivity, updating and monitoring. But there are systems out in the field which simple doesn’t fits in a single server, as the memory footprint is too large for scale-up systems

Of course, decision about scale-up or scale-out is in the most cases driven by the business requirements. This is on one site the deployed application like S/4 HANA or BW/4 HANA and on the other side a cost accepted decision, which deployment type is maybe more efficacy. In any cases the SAP support statement is decisive.

*Tags: Reference, SAP, SAP HANA, VMware, Scale-up, Scale-out*
