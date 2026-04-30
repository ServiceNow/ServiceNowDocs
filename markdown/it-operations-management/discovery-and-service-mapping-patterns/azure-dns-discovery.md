---
title: Azure DNS zones and record sets discovery using Patterns
description: The Discovery and Service Mapping Patterns application uses the Azure - DNS Zones \(LP\) and Azure - DNS Zone Recordsets \(LP\) Patterns to discover Azure Domain Name System \(DNS\) definitions \(zones and their respective record sets\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Azure, DNS, DNS zone, Azure DNS zone, Azure patterns, DNS record sets]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure DNS zones and record sets discovery using Patterns

The Discovery and Service Mapping Patterns application uses the Azure - DNS Zones \(LP\) and Azure - DNS Zone Recordsets \(LP\) Patterns to discover Azure Domain Name System \(DNS\) definitions \(zones and their respective record sets\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about Azure DNS zones and record sets and their version that you can discovery, refer to [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md).

For more information on Azure cloud discovery, see [Discovery for Microsoft Azure Cloud](../../discovery/concept/azure-cloud-discovery.md).

## Prerequisites

-   **Verify privileges**

    On the Microsoft Azure Console, provide a user with the API Management Service Reader role.

-   **Create Azure Service Principal credentials**

    For more information see: [Create Azure cloud credentials](../../discovery/task/create-azure-cloud-credentials.md).

-   **Configure Azure service account**

    For more information, see [Set up a cloud account for Azure](../../cloud-management-v2-setup/task/azure-cloud-accts-cloud-mgt.md).

-   **Create discovery schedule**

    Create a schedule for the relevant Azure service accounts. For more information, see [Create a discovery schedule in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - DNS Zones \(LP\) and Azure - DNS Zone Recordsets \(LP\) Patterns.

-   **Resources discovered by the Azure - DNS Zones \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the DNS Zone.|
    |Number Of RecordSets \[number\_of\_recordsets\]|The number of the recordsets defined within the DNS Zone.|
    |Operational status \[operational\_status\]|The operational status of the DNS Zone.|
    |State \[state\]|The state of the DNS Zone.|
    |Install Status \[install\_status\]|The install status of the DNS Zone.|
    |Comments \[comments\]|The field for general comments.|

-   **Resources discovered by the Azure - DNS Zone Recordsets \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the DNS alias record.|
    |IP Address \[ip\_address\]|IP address of the DNS alias record.|
    |Comments \[comments\]|Unique identifier for an Azure DNS zone combining service account ID, DNS zone name, and a fixed hash suffix.|
    |Operational status \[operational\_status\]|The operational status of the DNS alias record.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the DNS Name record.|
    |Operational status \[operational\_status\]|The operational status of the DNS record.|
    |Comments \[comments\]|Unique identifier for an Azure DNS zone combining service account ID, DNS zone name, and a fixed hash suffix.|


## CI relationships

These relationships are created to support Azure DNS zone discovery.

|CI|Relationship|CI|
|---|------------|---|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|DNS Zone \[cmdb\_ci\_dns\_zone\]|

These relationships are created to support Azure DNS zone record set discovery.

|CI|Relationship|CI|
|---|------------|---|
|DNS Zone \[cmdb\_ci\_dns\_zone\]|Contains::Contained by|DNS Name \[cmdb\_ci\_dns\_name\]|
|DNS Zone \[cmdb\_ci\_dns\_zone\]|Contains::Contained by|DNS Alias \[cmdb\_ci\_dns\_alias\]|
|DNS Name \[cmdb\_ci\_dns\_name\]|Used by::Uses|DNS Alias \[cmdb\_ci\_dns\_alias\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

