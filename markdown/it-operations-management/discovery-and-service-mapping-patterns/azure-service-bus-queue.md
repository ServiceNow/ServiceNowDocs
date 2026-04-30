---
title: Azure Service Bus Queue pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Azure, Discovery, ITOM, Pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Service Bus Queue pattern-based discovery

Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns](../service-mapping/reference/azure-cloud-discovery-patterns.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../service-mapping/task/activate-disabled-pattern.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](../it-operations-management/task/setup-azure-service-accounts.md).


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Service Bus Queue - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Enable Batched Operations \[enable\_batched\_operations\]|Indicates whether batched operations are enabled for the queue.|
|Enable Partitioning \[enable\_partitioning\]|Indicates whether message partitioning is enabled for load distribution across multiple message brokers.|
|DC Location \[location\]|The geographic region where the Service Bus queue is deployed.|
|Max Message Size In KB \[max\_message\_size\_in\_kb\]|The maximum allowed size of a single message in kilobytes \(KB\).|
|Max Size In MB \[max\_size\_in\_mb\]|The maximum storage size of the queue in megabytes \(MB\).|
|Object Id \[object\_id\]|The unique identifier for the Service Bus queue.|
|Resource Group \[resource\_group\]|Name of the resource group.|
|Subscription ID \[subscription\_id\]|The subscription ID.|
|Status \[status\]|The current status of the Service Bus queue.|
|Configuration Item \[configuration\_item\]|References the Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\] table.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Service Bus Queue - Extended Inventory\(LP\) pattern.

|Field|Description|
|-----|-----------|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Location \[location\]|The geographic region where the Service Bus queue is deployed.|
|Name \[name\]|The name of the Service Bus queue.|
|Object ID \[object\_id\]|The unique identifier for the Service Bus queue.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Type \[type\]|Type of resource. The value is set to **Microsoft.ServiceBus/namespaces/queues**.|

## CI relationships

The pattern creates these relationships to support discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Contains::Contained by|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|
|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure Service Bus - Queue \[cmdb\_azure\_service\_bus\_queue\]|References|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](../service-mapping/reference/azure-cloud-discovery-patterns.md)

