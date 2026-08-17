---
title: Azure NIC pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure network interfaces Controller \(NIC\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery-and-service-mapping-patterns/azure-nic-pattern.html
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 2
keywords: [Azure NIC, Azure network interface, Azure discovery, Azure patterns, NIC pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure NIC pattern-based discovery

Discovery and Service Mapping Patterns finds Azure network interfaces Controller \(NIC\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud components discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - NIC \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the network interface.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|MAC Address \[mac\_address\]|The MAC address of the network interface.|
|State \[state\]|The current state of the network interface.|
|NIC Status \[status\]|The provisioning state of the network interface as returned by Azure.|
|Private IP \[private\_ip\]|The IPv4 address of the network interface within the subnet.|
|Public IP \[public\_ip\]|The address of the Elastic IP address bound to the network interface.|
|Public DNS \[public\_dns\]|The public DNS name of the network interface.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - NIC \(LP\) pattern creates the following relationships and references to support Azure NIC discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

## Azure Tag discovery

The Azure - NIC \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table.|

**Parent Topic:**[Available discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

