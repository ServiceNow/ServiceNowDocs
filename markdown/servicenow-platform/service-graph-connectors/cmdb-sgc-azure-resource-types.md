---
title: Supported Microsoft Azure resource types
description: Several Microsoft Azure resource types are imported as CMDB data.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-10-14"
reading_time_minutes: 3
breadcrumb: [Reference, Microsoft Azure, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Supported Microsoft Azure resource types

Several Microsoft Azure resource types are imported as CMDB data.

Microsoft Azure resource types refer to the names included in delta queries used for filtering data using the [Azure Resource Graph](https://learn.microsoft.com/en-us/rest/api/azureresourcegraph/resourcegraph/resources/resources?view=rest-azureresourcegraph-resourcegraph-2022-10-01&tabs=HTTP) API for a specific data source.

**Note:** Delta pulls include data from a specific time period that is defined by the condition within a delta query.

The following table lists the Service Graph Connector for Microsoft Azure data sources, Microsoft Azure resource types they import, and indicates whether they support both full pull and delta pull of data during import. ✓ indicates supported and ✕ indicates not supported.

<table id="table_o2t_br4_q1c"><thead><tr><th>

Data source

</th><th>

CMDB CI classes

</th><th>

Microsoft Azure resource type

</th><th>

Full pull

</th><th>

Delta pull

</th></tr></thead><tbody><tr><td rowspan="2">

SG-Azure Subscriptions

</td><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

Microsoft.Resources/subscriptions

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

SG-Azure Datacenter Updation

</td><td>

Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Resource Group

</td><td>

Resource Group \[cmdb\_ci\_resource\_group\]

</td><td>

Microsoft.Resources/subscriptions/resourcegroups

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Availability Zone

</td><td>

Availability Zone \[cmdb\_ci\_availability\_zone\]

</td><td>

Microsoft.Compute/availabilitySets

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Storage Volume

</td><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

Microsoft.Compute/disks

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="3">

SG-Azure Load Balancers

</td><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Microsoft.Network/loadBalancers

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

</td><td>

Microsoft.Network/loadBalancers

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="4">

SG-Azure Network

</td><td>

Cloud Network \[cmdb\_ci\_network\]

</td><td>

Microsoft.Network/virtualnetworks

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

Microsoft.Network/virtualnetworks

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

</td><td>

Microsoft.Network/virtualnetworks

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="5">

SG-Azure Network Interface

</td><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Microsoft.Network/networkInterfaces

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td><td>

Microsoft.Network/networkInterfaces

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Microsoft.Network/networkInterfaces

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Microsoft.Network/networkInterfaces

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="5">

SG-Azure Public IP Address

</td><td>

Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]

</td><td>

Microsoft.Network/publicIPAddresses

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

Microsoft.Network/publicIPAddresses

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Microsoft.Network/publicIPAddresses

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

</td><td>

Microsoft.Network/publicIPAddresses

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Security Group

</td><td>

Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

</td><td>

Microsoft.Network/networkSecurityGroups

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Storage Accounts

</td><td>

Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]

</td><td>

Microsoft.Storage/storageAccounts

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="6">

SG-Azure Virtual Machines

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

Microsoft.Compute/virtualMachines

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

Microsoft.Compute/virtualMachines

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

Microsoft.Compute/virtualMachines

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]

</td><td>

Microsoft.Compute/virtualMachines

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Windows Server \[cmdb\_ci\_win\_server\]

</td><td>

Microsoft.Compute/virtualMachines

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Software

</td><td>

When the Software Asset Management \(SAM\) application isn't installed:

 Software \[cmdb\_ci\_spkg\]

 Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

When the SAM application is installed:

 Software Instance \[cmdb\_software\_instance\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure SQL

</td><td>

Cloud DataBase \[cmdb\_ci\_cloud\_database\]

</td><td>

Microsoft.Sql/serversMicrosoft.DBforPostgreSQL/servers

microsoft.dbformysql/flexibleservers

microsoft.dbforpostgresql/flexibleservers

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure TCP

</td><td>

TCP Connection \[cmdb\_tcp\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Running Process \[cmdb\_running\_process\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

SG-Azure Functions

</td><td>

Cloud Function \[cmdb\_ci\_cloud\_function\]

</td><td>

Microsoft.Web/sites

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure Generic Resources

</td><td>

Cloud Resource \[cmdb\_ci\_cmp\_resource\]

</td><td>

Microsoft.ResourceGraph/resources - Generic

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

SG-Azure Scale Sets

</td><td>

Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]

</td><td>

Microsoft.Compute/virtualmachinescalesets

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="10">

SG-Azure Scale Sets VMs**Note:** Imports uniform orchestration scale sets VMs.

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Server \[cmdb\_ci\_server\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Windows Server \[cmdb\_ci\_win\_server\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Tags

</td><td>

✓

</td><td>

✕

</td></tr><tr><td rowspan="2">

SG-Azure Software Remove

</td><td>

When the SAM application isn't installed:

 Software \[cmdb\_ci\_spkg\]

 Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

When the SAM application is installed:

 Software Instance \[cmdb\_software\_instance\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

SG-Azure Hardware Template Updation​

</td><td>

Hardware Type \[cmdb\_ci\_compute\_template\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td rowspan="2">

SG-Azure HW Consolidation​

</td><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

None

</td><td>

✓

</td><td>

✓

</td></tr><tr><td>

SG-Azure Run Command

</td><td>

None

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td rowspan="3">

SG-Azure Get Run Command

</td><td>

Application \[cmdb\_ci\_appl\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

TCP Connection \[cmdb\_tcp\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

Running Process \[cmdb\_running\_process\]

</td><td>

None

</td><td>

✓

</td><td>

✕

</td></tr><tr><td>

SG-Azure Kubernetes Cluster

</td><td>

SG-Azure Kubernetes Cluster \[sn\_sg\_azure\_integ\_kubernetes\_cluster\]

</td><td>

microsoft.containerservice/managedclusters

</td><td>

✓

</td><td>

✓

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for Microsoft Azure reference](../concept/sgc-azure-reference.md)

