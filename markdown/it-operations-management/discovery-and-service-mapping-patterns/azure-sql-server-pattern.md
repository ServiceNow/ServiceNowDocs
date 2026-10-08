---
title: Azure SQL Server pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure SQL Server virtual machines in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-sql-server-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 1
keywords: [Azure SQL Server, Azure discovery, Azure patterns, SQL Server pattern]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure SQL Server pattern-based discovery

Discovery and Service Mapping Patterns finds Azure SQL Server virtual machines in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - SQL Server \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|

## CI relationships and references

The Azure - SQL Server \(LP\) pattern creates the following relationships and references to support Azure SQL Server discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Azure License discovery

The pattern extension section discovers SQL Server license information and populates the license type in the Key Value \[cmdb\_key\_value\] table.

<table id="table_ojy_vss_5hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

SQL\_Server\_License\_Type\_automatic

</td></tr><tr><td>

Value \[value\]

</td><td>

The license model, which is one of the following: -   Azure Hybrid Benefit: **BYOL**
-   Pay-as-you-go licensing: **License Included**

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/azure-cloud-discovery-patterns.md)

