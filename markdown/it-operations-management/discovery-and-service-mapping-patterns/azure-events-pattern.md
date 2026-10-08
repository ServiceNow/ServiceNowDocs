---
title: Azure Events pattern-based discovery
description: Discovery uses event patterns to update Microsoft Azure Cloud component data in near real-time. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-events-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 6
keywords: [Azure Events, Azure event discovery, Azure patterns]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Events pattern-based discovery

Discovery uses event patterns to update Microsoft Azure Cloud component data in near real-time. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md).

## Verify the REST API permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Events discovered by Discovery during horizontal discovery

Discovery uses patterns to find events created for Microsoft Azure Cloud components. If there are events that indicate the change of state in one of the Microsoft Azure Cloud components, it triggers the discovery of Microsoft Azure Cloud components using the patterns.

|Pattern|CI|
|-------|---|
|Azure Application LB Event|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Azure Availability Set Event|Availability Set \[cmdb\_ci\_availability\_set\]|
|Azure Classic LB Event|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Azure DataBase Event|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|Azure Express Route Circuit Event|Cloud Direct Connect \[cmdb\_ci\_cloud\_direct\_connect\]|
|Azure Functions Event|Cloud Function \[cmdb\_ci\_cloud\_function\]|
|Azure Local Network Gateway Event|Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|
|Azure NAT Gateway Event|NAT Gateway \[cmdb\_ci\_nat\_gateway\]|
|Azure Network Event|Cloud Network \[cmdb\_ci\_network\]|
|Azure NIC Event|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Azure Private DNS Zone Event|DNS Zone \[cmdb\_ci\_dns\_zone\]|
|Azure Public IP Event|Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|
|Azure Resource Group Event|Resource Group \[cmdb\_ci\_resource\_group\]|
|Azure Security Group Event|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Azure Storage Account Event|Cloud Storage Account \[cmdb\_ci\_cloud\_storage\_account\]|
|Azure Virtual Machine Event|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Azure Virtual Network Gateway Connection Event|Virtual Network Gateway Connection \[cmdb\_ci\_vpc\_gateway\_connection\]|
|Azure Virtual Network Peerings Event|Virtual Network Peering \[cmdb\_ci\_vnet\_peering\]|
|Azure VM Scale Set Event|Instance Scale Set \[cmdb\_ci\_instance\_scale\_set\]|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)

**Related topics**  


[Azure Application LB pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-application-lb-pattern.md)

[Azure availability sets discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-availability-sets-patterns.md)

[Azure Classic Load Balancer pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-classic-load-balancer-pattern.md)

[Azure Database pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-database-pattern.md)

[Azure Express Route Circuit pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-express-route-circuit-pattern.md)

[Microsoft Azure Functions discovery with Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-function-discovery.md)

[Azure Local Network Gateway pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-local-network-gateway-pattern.md)

[Azure NAT Gateway pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-nat-gateway-pattern.md)

[Azure Network and Subnet pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-network-subnet-pattern.md)

[Azure NIC pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-nic-pattern.md)

[Azure Private DNS Zone pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-private-dns-zone-pattern.md)

[Azure Public IP pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-public-ip-pattern.md)

[Azure Resource Group pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-resource-group-pattern.md)

[Azure Security Group pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-security-group-pattern.md)

[Azure Storage Account pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-storage-account-pattern.md)

[Azure virtual machine pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-vm-pattern.md)

[Azure Virtual Network Gateway Connection pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/azure-vng-connection-pattern.md)

[Azure Virtual Machine Scale Sets \(VMSS\) Instance discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/AzureVMScaleSetInstance.md)

