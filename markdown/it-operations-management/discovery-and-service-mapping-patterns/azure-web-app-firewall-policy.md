---
title: Azure Web Application Firewall Policy pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 3
keywords: [Azure, Discovery, ITOM, Pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Web Application Firewall Policy pattern-based discovery

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

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Azure - Web Application Firewall Policy - Extended Inventory\(LP\) pattern.

You can review the non-CMDB Azure tables by navigating to **All** &gt; **Configuration** &gt; **Azure**. You can also search the navigation filter for the specific pattern name.

|Field|Description|
|-----|-----------|
|Object Id \[object\_id\]|The unique identifier of the resource.|
|Kind \[kind\]|The specific kind or variant of the resource.|
|DC Location \[location\]|The Azure region where the resource is deployed.|
|Resource Group \[resource\_group\]|The name of the resource group containing the resource.|
|Subscription Id \[subscription\_id\]|The subscription ID associated with the resource.|
|Tenant Id \[tenant\_id\]|The Azure Active Directory tenant ID associated with the resource.|
|Provisioning State \[provisioning\_state\]|The latest provisioning status of the resource.|
|Configuration Item \[configuration\_item\]|References the Web ACL \[cmdb\_ci\_web\_acl\] table.|
|Policy State \[policy\_state\]|The current state of the policy applied to the resource.|

## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Azure - Web Application Firewall Policy - Extended Inventory\(LP\) pattern.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

The unique identifier of the resource.

</td></tr><tr><td>

Name \[name\]

</td><td>

The name of the resource.

</td></tr><tr><td>

Location \[location\]

</td><td>

The Azure region where the resource is deployed.

</td></tr><tr><td>

Default Action \[default\_action\]

</td><td>

Indicates the effective operation mode of the web application firewall \(WAF\) policy. Possible values are allow and detect.-   allow: policy is running in **Prevention** mode and is blocking traffic
-   detect: policy is running in **Detection** mode and is logging only

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Type of resource. The value is set to **microsoft.network/applicationgatewaywebapplicationfirewallpolicies**.

</td></tr></tbody>
</table>## CI relationships

The Azure - Web Application Firewall Policy - Extended Inventory\(LP\) pattern creates these relationships to support Azure Web Application Firewall Policy discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Protected by::Protects|Web ACL \[cmdb\_ci\_web\_acl\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Web ACL \[cmdb\_ci\_web\_acl\]|
|Web ACL \[cmdb\_ci\_web\_acl\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure Web Application Firewall - Policy \[cmdb\_azure\_web\_application\_firewall\_policy\]|References|Web ACL \[cmdb\_ci\_web\_acl\]|

## Azure tag discovery

The pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](../service-mapping/reference/azure-cloud-discovery-patterns.md)

