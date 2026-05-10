---
title: Microsoft Azure discovery solutions comparison
description: ITOM Visibility applications discover a variety of Microsoft Azure resources and populate the relevant configuration item \(CI\) classes in the Configuration Management Database \(CMDB\) with their attributes.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Patterns, Azure, Cloud, Discovery, Visibility, CMDB, Service Graph Connector, Configuration item]
breadcrumb: [Cloud discovery solutions comparison, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure discovery solutions comparison

ITOM Visibility applications discover a variety of Microsoft Azure resources and populate the relevant configuration item \(CI\) classes in the Configuration Management Database \(CMDB\) with their attributes.

## ITOM Visibility solutions

ITOM Visibility can offer you comprehensive visibility into your organization's cloud infrastructure. Each application offers unique strengths and capabilities, and by comparing them you can gain holistic insights on their capabilities and benefits.

<table id="table_sld_tvh_hfc"><thead><tr><th>

ITOM Visibility solution

</th><th>

Overview

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

Discovery and Service Mapping Patterns and Visibility Content

</td><td>

[Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md)

</td><td>

-   You must update your store apps to the latest release version.
-   You must provide ITOM Visibility with access permissions. For more information, see [Set up Azure service accounts](../task/setup-azure-service-accounts.md)

</td></tr><tr><td>

Service Graph Connector for Microsoft Azure

</td><td>

[Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-integration-azure.md)

</td><td>

[Configure Service Graph Connector for Microsoft Azure using the guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/configure-azure-integration.md)

</td></tr></tbody>
</table>**Note:**

The CI class, in most cases, is applicable to both solutions. If it's not applicable to one of the solutions, the solution is marked "N/A".

<table id="table_jqp_vgh_hfc"><thead><tr><th>

Resource type

</th><th>

Supported by Cloud Discovery and Service Mapping Patterns

</th><th>

Supported by Cloud Service Graph Connectors

</th><th>

CI Class

</th></tr></thead><tbody><tr><td>

microsoft.compute/availabilitysets

</td><td>

Yes

</td><td>

N/A

</td><td>

cmdb\_ci\_availability\_set

</td></tr><tr><td>

microsoft.compute/availabilitysets

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_availability\_zone

</td></tr><tr><td>

Microsoft.Management/managementGroups

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_azure\_management\_group

</td></tr><tr><td>

microsoft.KeyVault/vaults

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_certificate

</td></tr><tr><td>

-   Microsoft.Sql/servers/databases
-   Microsoft.DBforMySQL/servers
-   Microsoft.DocumentDB/databaseAccounts
-   Microsoft.Cache/Redis

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_database

</td></tr><tr><td>

-   Microsoft.Sql/servers
-   Microsoft.DBforPostgreSQL/servers

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_cloud\_database

</td></tr><tr><td>

microsoft.network/expressroutecircuits

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_direct\_connect

</td></tr><tr><td>

Microsoft.Storage/storageAccounts/fileServices

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_file\_service

</td></tr><tr><td>

Microsoft.Storage/storageAccounts/fileServices/shares

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_file\_share

</td></tr><tr><td>

Microsoft.Web/sites/functions

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_cloud\_function

</td></tr><tr><td>

VM Size

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_hardware\_type

</td></tr><tr><td>

microsoft.compute/hostgroups/hosts

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_host

</td></tr><tr><td>

microsoft.network/applicationgateways

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_load\_balancer

</td></tr><tr><td>

microsoft.network/loadbalancers

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_cloud\_load\_balancer

</td></tr><tr><td>

Microsoft.Storage/storageAccounts/blobService

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_object\_service

</td></tr><tr><td>

Tenant

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_org

</td></tr><tr><td>

microsoft.network/publicipaddresses

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_cloud\_public\_ipaddress

</td></tr><tr><td>

Microsoft.Storage/storageAccounts/queueServices

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_queue\_service

</td></tr><tr><td>

Microsoft.Resources/subscriptions

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_cloud\_service\_account

</td></tr><tr><td>

Microsoft.Management/managementGroup

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_service\_account

</td></tr><tr><td>

microsoft.storage/storageaccounts

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_cloud\_storage\_account

</td></tr><tr><td>

Microsoft.Network/virtualNetworks/subnets

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_subnet

</td></tr><tr><td>

Microsoft.Storage/storageAccounts/tableServices

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_table\_service

</td></tr><tr><td>

microsoft.web/sites

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_cloud\_webserver

</td></tr><tr><td>

microsoft.network/networksecuritygroups

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_compute\_security\_group

</td></tr><tr><td>

microsoft.network/privatednszones

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_dns\_zone

</td></tr><tr><td>

microsoft.compute/virtualmachinescalesets

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_instance\_scale\_set

</td></tr><tr><td>

microsoft.containerservice/managedclusters

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_kubernetes\_cluster

</td></tr><tr><td>

Microsoft.Network/loadBalancers/backendAddressPools

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_lb\_pool

</td></tr><tr><td>

Microsoft.Network/loadBalancers/inboundNatRules

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_lb\_service

</td></tr><tr><td>

microsoft.network/natgateways

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_nat\_gateway

</td></tr><tr><td>

microsoft.network/virtualnetworks

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_network

</td></tr><tr><td>

microsoft.network/networkinterfaces

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_nic

</td></tr><tr><td>

microsoft.compute/images

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_os\_template

</td></tr><tr><td>

Microsoft.Resources/resourceGroups

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_resource\_group

</td></tr><tr><td>

Microsoft.Network/routeTables/routes

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_route\_table

</td></tr><tr><td>

microsoft.network/routetables

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_route\_table

</td></tr><tr><td>

microsoft.compute/disks

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_storage\_volume

</td></tr><tr><td>

microsoft.network/localnetworkgateways

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_virtual\_pvt\_gateway

</td></tr><tr><td>

microsoft.network/virtualnetworkgateways

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_virtual\_pvt\_gateway

</td></tr><tr><td>

microsoft.compute/virtualmachines

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_vm\_instance

</td></tr><tr><td>

microsoft.sqlvirtualmachine/sqlvirtualmachines

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_vm\_instance

</td></tr><tr><td>

Microsoft.Network/virtualNetworks/virtualNetworkPeerings

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_vnet\_peering

</td></tr><tr><td>

microsoft.network/connections

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_ci\_vpc\_gateway\_connection

</td></tr><tr><td>

Microsoft.Resources/tags

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_key\_value

</td></tr><tr><td>

Microsoft.Compute/virtualMachines

</td><td>

No

</td><td>

Yes

</td><td>

cmdb\_ci\_server

</td></tr><tr><td>

Microsoft.Compute/virtualMachines

</td><td>

No

</td><td>

Yes

</td><td>

cmdb\_ci\_win\_server

</td></tr><tr><td>

Microsoft.Network/networkInterfaces

</td><td>

No

</td><td>

Yes

</td><td>

cmdb\_ci\_hardware

</td></tr><tr><td>

Microsoft.Compute/virtualMachines

</td><td>

No

</td><td>

Yes

</td><td>

cmdb\_ci\_linux\_server

</td></tr><tr><td>

microsoft.containerservice/managedclusters

</td><td>

Yes

</td><td>

Yes

</td><td>

cmdb\_ci\_kubernetes\_cluster

</td></tr><tr><td>

Microsoft.Compute/virtualmachinescalesets

</td><td>

No

</td><td>

Yes

</td><td>

cmdb\_ci\_vm\_instance

</td></tr><tr><td>

Microsoft.ServiceBus/namespaces/queues

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_service\_bus\_queue

</td></tr><tr><td>

Microsoft.ServiceBus/namespaces/topics

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_service\_bus\_topic

</td></tr><tr><td>

microsoft.appconfiguration/configurationstores

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_app\_configuration\_configuration\_store

</td></tr><tr><td>

microsoft.automation/automationaccounts

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_automation\_automation\_account

</td></tr><tr><td>

microsoft.compute/diskencryptionsets

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_disk\_encryption\_set\_disk\_encryption\_set

</td></tr><tr><td>

microsoft.compute/galleries/images

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_compute\_gallery\_image\_definition

</td></tr><tr><td>

microsoft.compute/snapshots

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_compute\_snapshot

</td></tr><tr><td>

microsoft.containerregistry/registries

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_container\_registry\_registry

</td></tr><tr><td>

microsoft.databricks/workspaces

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_databricks\_workspace

</td></tr><tr><td>

microsoft.datafactory/factories

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_data\_factory\_data\_factory

</td></tr><tr><td>

microsoft.dataprotection/backupvaults

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_data\_protection\_backup\_vault

</td></tr><tr><td>

microsoft.eventgrid/systemtopics

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_event\_grid\_system\_topic

</td></tr><tr><td>

microsoft.eventhub/namespaces

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_event\_hub\_namespace

</td></tr><tr><td>

microsoft.insights/components

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_application\_insight\_component

</td></tr><tr><td>

microsoft.network/applicationgatewaywebapplicationfirewallpolicies

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_web\_application\_firewall\_policy

</td></tr><tr><td>

microsoft.operationalinsights/workspaces

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_log\_analytics\_workspace

</td></tr><tr><td>

microsoft.network/azurefirewalls

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_network\_security\_azure\_firewall

</td></tr><tr><td>

microsoft.devcenter/devcenters

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_dev\_centers\_dev\_center

</td></tr><tr><td>

microsoft.kusto/clusters

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_data\_explorer\_clusters\_data\_explorer\_clusters

</td></tr><tr><td>

microsoft.recoveryservices/vaults

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_recovery\_services\_vault

</td></tr><tr><td>

microsoft.recoveryservices/vaults/backupfabrics/protectioncontainers/protecteditems

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_recovery\_services\_vault\_backup\_item

</td></tr><tr><td>

microsoft.dbforpostgresql/servergroupsv2

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_cosmos\_db\_for\_postgresql\_cluster\_cluster

</td></tr><tr><td>

microsoft.insights/datacollectionrules

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_application\_insight\_data\_collection\_rule

</td></tr><tr><td>

microsoft.network/serviceendpointpolicies

</td><td>

Yes

</td><td>

No

</td><td>

cmdb\_azure\_service\_endpoint\_policy\_service\_endpoint\_policy

</td></tr></tbody>
</table>**Parent Topic:**[Cloud discovery solutions comparison](../concept/cloud-discovery-methods-comparison.md)

