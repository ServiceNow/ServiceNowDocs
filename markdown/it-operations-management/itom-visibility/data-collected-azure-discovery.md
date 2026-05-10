---
title: Data collected for Microsoft Azure Cloud Discovery
description: Discovery collects information about cloud resources in Microsoft Azure datacenters. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Patterns]
breadcrumb: [Cloud resource discovery references, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Data collected for Microsoft Azure Cloud Discovery

Discovery collects information about cloud resources in Microsoft Azure datacenters. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
    -   Visibility Content
-   **Create Azure cloud credentials**

    Create Microsoft Azure credentials that can access the Microsoft Azure account. For more information, see [Create Azure cloud credentials](../task/create-azure-cloud-credentials.md).

-   **Configure a discovery schedule**

    [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md)


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## How Discovery finds Microsoft Azure resources

Discovery uses the Cloud Provisioning and Governance API and Discovery and Service Mapping Patterns to find cloud resources.

<table id="table_wwr_rng_gz"><thead><tr><th>

Pattern

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Azure DataBase \(LP\)

</td><td>

Discovers database types of:

-   Microsoft.sql/servers
-   microsoft.sql/managedInstances
-   microsoft.dbformysql
-   microsoft.documentdb/databaseaccounts
-   microsoft.cache/redis
-   microsoft.dbforpostgresql/servers
-   microsoft.dbformysql/servers
-   microsoft.dbformysql/flexibleservers
-   microsoft.dbforpostgresql/flexibleservers

 Populates the \[cmdb\_ci\_cloud\_database\] table.

</td></tr><tr><td>

Azure LoadBalancer TD

</td><td>

Retrieves Microsoft Azure load balancers and populates the cmdb\_ci\_lb\_service table. This pattern is only used by Service Mapping for top-down discovery, not by the Discovery application for horizontal discovery.

</td></tr><tr><td>

Azure WebSite \(LP\)

</td><td>

Retrieves Microsoft Azure web servers and populates the Cloud WebServers \[cmdb\_ci\_cloud\_webserver\] and IP address \[cmdb\_ci\_ip\_address\] tables.

</td></tr></tbody>
</table>## Data collected by Discovery during horizontal discovery

|Label|Field Name|
|-----|----------|
|Name|name|
|Region|region|
|Object ID|object\_id|

|Label|Field Name|
|-----|----------|
|Name|name|

|Label|Field Name|
|-----|----------|
|Name|name|
|State|state|
|Object ID|object\_id|
|CPUs|cpus|
|Disks|disks|
|Disks size \(GB\)|disks\_size|
|Memory|memory|
|Network adapters|nics|
|VM Instance ID|vm\_inst\_id|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|State|state|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Guest OS|guest\_os|
|Image source|image\_source|

|Label|Field Name|
|-----|----------|
|Name|name|
|State|state|
|Object ID|object\_id|
|Storage type|storage\_type|
|Size|size|

|Label|Field Name|
|-----|----------|
|Name|name|
|State\*|state|
|CIDR\*|cidr|

\*Not found on VMware vCenter networks.

|Label|Field Name|
|-----|----------|
|Name|name|
|Status|status|
|CIDR|cidr|

|Label|Field Name|
|-----|----------|
|Name|name|
|Netmask|netmask|
|MAC Address|mac\_address|
|MAC Manufacturer|mac\_manufacturer|
|Status|install\_status|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|State|state|

|Label|Field Name|
|-----|----------|
|Name|name|
|Provisioning state|provisioning\_state|

**Note:** This table is only available for Discovery when the Cloud Provisioning and Governance plugin is activated.

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|State|state|
|Operational Status|operational\_status|
|Install Status|install\_status|

**Note:**

-   When a resource group is discovered for the first time, the **State** field is set to **Available**, **operational\_status=Operational**, and **Status=Installed**; based on the response mapping.
-   When a resource group is terminated on Microsoft Azure, the CMPReconciler scripts set the **State** field to **Terminated**, and **operational\_status=Non-Operational** and **Status=Absent**.

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Public IP address|public\_ip\_address|
|Public DNS|public\_dns|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Sku Name|sku\_name|
|State|state|

<table id="table_wbh_k4s_mbb"><thead><tr><th>

Label

</th><th>

Field Name

</th></tr></thead><tbody><tr><td>

Fully qualified domain name

</td><td>

fqdn

</td></tr><tr><td>

Name

</td><td>

name

</td></tr><tr><td>

Object ID

</td><td>

object\_id

</td></tr><tr><td>

Operational Status

</td><td>

operational\_status

</td></tr><tr><td>

Type

</td><td>

type

</td></tr><tr><td>

State

</td><td>

state

</td></tr><tr><td>

Vendor

</td><td>

vendor

</td></tr><tr><td>

Version

</td><td>

version**Note:** For NoSQL and MSSQL Managed Instances, the API responses for these databases do not return version data.

</td></tr><tr><td>

Category

</td><td>

category

</td></tr></tbody>
</table>|Label|Field Name|
|-----|----------|
|Name|name|
|Install status|install\_status|
|Vendor|vendor|
|Fully qualified domain name|fqdn|
|Operational status|operational\_status|
|State|state|

|Label|Field Name|
|-----|----------|
|Fully qualified domain name|fqdn|
|Install status|install\_status|
|IP Address|ip\_address|
|Name|name|
|Netmask|netmask|
|Operational status|operational\_status|
|Vendor|vendor|

|Label|Field Name|
|-----|----------|
|Life-cycle Stage Status|life\_cycle\_stage\_status|
|Name|name|
|Status|status|
|Serial Number|serial\_number|
|Type|type|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|VCPUS|vcpus|

|Label|Field Name|
|-----|----------|
|Name|name|
|Object ID|object\_id|
|Provider|provider|
|vCPUs|vcpus|

**Parent Topic:**[Cloud resource discovery references](cloud-discovery-collected-data.md)

**Related topics**  


[Microsoft Azure Cloud discovery using patterns](../../service-mapping/reference/azure-cloud-discovery-patterns.md)

[Service Graph Connector for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-integration-azure.md)

[Agent Client Collector Discovery](../../agent-client-collector/concept/acc-discovery.md)

