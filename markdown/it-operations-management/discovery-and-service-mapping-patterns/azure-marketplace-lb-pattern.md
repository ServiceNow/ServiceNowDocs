---
title: Azure Marketplace pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Marketplace products in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-marketplace-lb-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-18"
reading_time_minutes: 3
keywords: [Azure Marketplace, Azure discovery, Azure patterns, Marketplace pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Marketplace pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Marketplace products in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Azure - Marketplace LB \(LP\) pattern discovers the following Azure Marketplace products:

-   SaaS
-   Azure Application
-   Virtual Machine

    **Note:** The pattern discovers only virtual machines \(VMs\) created from third-party or commercial marketplace images.


## Azure Marketplace data model

The Azure - Marketplace LB \(LP\) pattern introduces the following CI class that extends an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Marketplace LB \(LP\) pattern.

<table id="table_deployed_marketplace"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Cloud resource, usually the marketplace offering or SKU name.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

A unique resource ID of the Cloud resource.

</td></tr><tr><td>

Resource Type \[resource\_type\]

</td><td>

The type of the resource in the Cloud Marketplace. For example: `microsoft.compute/virtualmachines`.

</td></tr><tr><td>

Plan Name \[plan\_name\]

</td><td>

Billing or SKU plan for a resource from the Cloud Marketplace.For example: Pay as You Go.

</td></tr><tr><td>

Market \[market\]

</td><td>

International Organization for Standardization \(ISO\) code of the geographical market where the resource is sold. For example: US or EU.

</td></tr><tr><td>

Organization Id \[organization\_id\]

</td><td>

A unique identifier for the organization or publisher that owns the marketplace resource.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Product Code \[product\_code\]|A unique product code of the resource within the Cloud Marketplace.|
|Publisher Name \[publisher\_name\]|The organization or individual responsible for creating and offering the product or service.|
|Version \[version\]|Release number or iteration of the product.|
|Deployed On \[deployed\_on\]|References the Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\] table.|

## CI relationships and references

The Azure - Marketplace LB \(LP\) pattern creates the following relationships and references to support Azure Marketplace discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|
|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]\*|

\* This relationship is created only for resources with a global region.

|CI|Field|Referenced CI|
|---|-----|-------------|
|Marketplace Product Details \[marketplace\_product\_details\]|Deployed On \[deployed\_on\]|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|

## Azure Tag discovery

The Azure - Marketplace LB \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\] table.|

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)

