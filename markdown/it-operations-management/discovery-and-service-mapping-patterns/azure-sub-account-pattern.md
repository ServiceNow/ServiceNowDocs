---
title: Azure sub account pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure subscriptions and management groups on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-sub-account-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 4
keywords: [Azure Sub Account, Azure discovery, Azure Management Groups, Azure patterns, Sub Account pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure sub account pattern-based discovery

Discovery and Service Mapping Patterns finds Azure subscriptions and management groups on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Azure Management Groups data model

The Azure Management Groups pattern extension introduces the following CI class that extends an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|Configuration Item \[cmdb\_ci\]|

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Sub Account \(LP\) pattern.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the subscription or service account.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The subscription ID, allocated by Azure for this resource.

</td></tr><tr><td>

Account Id \[account\_id\]

</td><td>

The subscription ID of the service account.

</td></tr><tr><td>

Datacenter Type \[datacenter\_type\]

</td><td>

Type of datacenter associated with the service account. The value is set to **cmdb\_ci\_azure\_datacenter**.

</td></tr><tr><td>

Datacenter URL \[datacenter\_url\]

</td><td>

The URL of the datacenter associated with the service account.

</td></tr><tr><td>

Is management account \[is\_master\_account\]

</td><td>

Boolean attribute indicating whether this is the management account. The value is set to **false** for discovered sub-accounts.

</td></tr><tr><td>

Discovery credentials \[discovery\_credentials\]

</td><td>

Reference field to the related Azure credentials.

</td></tr><tr><td>

Parent account \[parent\_account\]

</td><td>

Reference to the primary account, if it exists.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the subscription, derived from its Azure state. For example: Operational or Non-Operational.

</td></tr><tr><td>

Life Cycle Stage \[life\_cycle\_stage\]

</td><td>

Life cycle stage of the subscription, derived from its Azure state. For example: Operational, End of Operation, or End of Life.

</td></tr><tr><td>

Life Cycle Stage Status \[life\_cycle\_stage\_status\]

</td><td>

Life cycle stage status of the subscription, derived from its Azure state. For example: In Use, Action Required, On Hold, Billing Past Due, or Retired.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr></tbody>
</table>Discovery populates the data in the CMDB when running the Azure Management Groups pattern extension.

<table id="table_azure_management_group"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Management group name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Management group name and tenant ID in the following format: `name+@+tenantId`. For example: itomMgmtGroup@8bcff-vdc-btrv.

</td></tr><tr><td>

Parent \[parent\]

</td><td>

References the direct parent Azure Management Group \[cmdb\_ci\_azure\_management\_group\] table.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table><table id="table_cloud_org"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Tenant ID or name. -   Tenant ID: When using management-level credentials
-   Tenant name: When using tenant-level credentials

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Tenant ID.

</td></tr><tr><td>

DNS Domain \[dns\_domain\]

</td><td>

Domain name entered during registration, for example: servicenow.com. This field is populated only when tenant-level credentials are used.

</td></tr></tbody>
</table>## CI relationships and references

The Azure - Sub Account \(LP\) pattern creates the following references to support Azure Sub Account discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

The Azure Management Groups pattern extension creates the following relationships and references to support Azure Sub Account discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|
|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|Contains::Contained by|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]|Parent \[parent\]|Azure Management Group \[cmdb\_ci\_azure\_management\_group\]\*|

\* Only references the direct parent-child management group relationship.

## Azure Tag discovery

The Azure - Sub Account \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)

