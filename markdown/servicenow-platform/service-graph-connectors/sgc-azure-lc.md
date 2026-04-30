---
title: Life cycle management of records in Service Graph Connector for Microsoft Azure
description: Life cycle management in the Service Graph Connector for Microsoft Azure monitors and updates the statuses of Azure resources throughout their entire life cycle, from creation to deletion.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-10-12"
reading_time_minutes: 2
breadcrumb: [Reference, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle management of records in Service Graph Connector for Microsoft Azure

Life cycle management in the Service Graph Connector for Microsoft Azure monitors and updates the statuses of Azure resources throughout their entire life cycle, from creation to deletion.

The life cycle management process helps maintain the accuracy and integrity of data in the Configuration Management Database \(CMDB\).

## Life cycle management for CIs in Service Graph Connector for Microsoft Azure

The following table lists the configuration items \(CIs\) in CMDB and other non-CMDB tables for which life cycle management is available in Service Graph Connector for Microsoft Azure.

<table id="table_j2z_xvz_ncc"><thead><tr><th>

Data source

</th><th>

CMDB CI classes

</th><th>

Life cycle management available

</th></tr></thead><tbody><tr><td rowspan="2">

SG-Azure Availability Zone

</td><td>

Availability Zone \[cmdb\_ci\_availability\_zone\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td>

SG-Azure Datacenter Updation

</td><td>

Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-Azure Functions

</td><td>

Cloud Function \[cmdb\_ci\_cloud\_function\]

</td><td>

Yes

</td></tr><tr><td rowspan="2">

SG-Azure Generic Resources

</td><td>

Cloud Resource \[cmdb\_ci\_cmp\_resource\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="3">

SG-Azure Get Run Command

</td><td>

Application \[cmdb\_ci\_appl\]

</td><td>

Not applicable

</td></tr><tr><td>

TCP Connection \[cmdb\_tcp\]

</td><td>

Not applicable

</td></tr><tr><td>

Running Process \[cmdb\_running\_process\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-Azure Hardware Template Updation​

</td><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

Not applicable

</td></tr><tr><td rowspan="2">

SG-Azure HW Consolidation​

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Not applicable

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Not applicable

</td></tr><tr><td>

SG-Azure Kubernetes Cluster

</td><td>

Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]

</td><td>

Yes

</td></tr><tr><td rowspan="3">

SG-Azure Load Balancers

</td><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Yes

</td></tr><tr><td>

Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="4">

SG-Azure Network

</td><td>

Cloud Network \[cmdb\_ci\_network\]

</td><td>

Yes

</td></tr><tr><td>

Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

</td><td>

Yes

</td></tr><tr><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

No

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="5">

SG-Azure Network Interface

</td><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Yes

</td></tr><tr><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td><td>

No

</td></tr><tr><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Not applicable

</td></tr><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Not applicable

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="5">

SG-Azure Public IP Address

</td><td>

Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]

</td><td>

Yes

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Yes

</td></tr><tr><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Yes

</td></tr><tr><td>

Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="2">

SG-Azure Resource Group

</td><td>

Resource Group \[cmdb\_ci\_resource\_group\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td>

SG-Azure Scale Sets

</td><td>

Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

</td><td>

Yes

</td></tr><tr><td rowspan="9">

SG-Azure Scale Sets VMs

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Yes

</td></tr><tr><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Yes

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

Not applicable

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Yes

</td></tr><tr><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

Not applicable

</td></tr><tr><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

Yes

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]

</td><td>

Yes

</td></tr><tr><td>

Windows Server \[cmdb\_ci\_win\_server\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="2">

SG-Azure Security Group

</td><td>

Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td>

SG-Azure Software

</td><td>

When the Software Asset Management \(SAM\) application isn't installed:

 Software \[cmdb\_ci\_spkg\]

 Software Instance \[cmdb\_software\_instance\]

 When the SAM application is installed:

 Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Yes

</td></tr><tr><td>

SG-Azure Software Remove

</td><td>

When the SAM application isn't installed:

 Software \[cmdb\_ci\_spkg\]

 Software Instance \[cmdb\_software\_instance\]

 When the SAM application is installed:

 Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Yes

</td></tr><tr><td rowspan="2">

SG-Azure SQL

</td><td>

Cloud DataBase \[cmdb\_ci\_cloud\_database\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="2">

SG-Azure Storage Accounts

</td><td>

Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="2">

SG-Azure Storage Volume

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="2">

SG-Azure Subscriptions

</td><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

No

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td rowspan="2">

SG-Azure TCP

</td><td>

TCP Connection \[cmdb\_tcp\]

</td><td>

No

</td></tr><tr><td>

Running Process \[cmdb\_running\_process\]

</td><td>

No

</td></tr><tr><td rowspan="6">

SG-Azure Virtual Machines

</td><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

Yes

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]

</td><td>

Yes

</td></tr><tr><td>

Windows Server \[cmdb\_ci\_win\_server\]

</td><td>

Yes

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

Yes

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

No

</td></tr><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Yes

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for Microsoft Azure reference](sgc-azure-reference.md)

