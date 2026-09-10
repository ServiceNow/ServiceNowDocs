---
title: Improved query performance with direct field population in CI tables
description: The Populate Service Account and LDC IN CMDB scheduled job populates the Service Account and Logical Datacenter fields in cloud configuration item \(CI\) tables, and the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. This direct population reduces query complexity and improves query performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/query-service-account-ldc-fields.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [cloud CI tables, Service Account, Logical Datacenter, query performance, cloud discovery]
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Improved query performance with direct field population in CI tables

The **Populate Service Account and LDC IN CMDB** scheduled job populates the Service Account and Logical Datacenter fields in cloud configuration item \(CI\) tables, and the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. This direct population reduces query complexity and improves query performance.

Cloud Service Account and Logical Datacenter information is stored separately from cloud CIs. To retrieve account or datacenter information for a cloud resource, queries require joins across multiple tables, including the relationship table that connects CIs. Similarly, Virtual Machine Object information is stored separately from the Hardware CI, requiring additional joins to retrieve data from the Virtual Machine Object \[cmdb\_ci\_vm\_object\] table. With potentially millions of records in the relationship table, these joins could increase query time for teams working with cloud infrastructure data.

Starting with the Discovery and Service Mapping Patterns version 1.30.2, you can enable a feature that denormalizes cloud CI tables by populating the **Service Account** \[cloud\_service\_account\] and **Logical Datacenter** \[logical\_datacenter\] fields directly in cloud CI tables. The scheduled job also references tables extended from the Virtual Machine Object \[cmdb\_ci\_vm\_object\] table via the Virtual Machine Object reference field in the Hardware \[cmdb\_ci\_hardware\] table. Populating these fields directly reduces the need for complex joins, supporting more efficient queries for reporting, analytics, and operational workflows involving cloud resources. After you enable this feature, Discovery populates these fields for both existing and newly discovered CIs.

\[Omitted image "multi-joins-vs-direct-fields.png"\] Alt text: Comparison between complex multi-table joins without the feature versus direct field access with the feature

For information about enabling this feature, see [Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md).

## System properties

<table id="table_job_properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_itom\_pattern.populate\_saldc.stale\_job\_threshold\_days**

</td><td>

Sets the number of days after which a running job is considered stale and automatically canceled. For more information, see [Set the Populate Service Account and LDC job stale threshold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-stale-days.md).-   **Type**: Integer
-   **Default value**: 2

</td></tr><tr><td>

**sn\_itom\_pattern.populate\_saldc\_full\_resync**

</td><td>

Starting with Discovery and Service Mapping Patterns version 1.35.0, determines if all CI records are reprocessed on the next job run. For more information, see [Trigger a full CI table resync for direct field population](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-full-resync.md).-   **Type**: Boolean
-   **Default value**: False

</td></tr></tbody>
</table>## Supported Cloud CI tables

Service Account and Logical Datacenter fields are added to the following cloud CI tables:

|Table label|Table name|
|-----------|----------|
|Cloud Subnet|cmdb\_ci\_cloud\_subnet|
|Cloud Network|cmdb\_ci\_network|
|Virtual Machine Instance|cmdb\_ci\_vm\_instance|
|Hardware Type|cmdb\_ci\_compute\_template|
|Cloud Hardware Type|cmdb\_ci\_cloud\_hardware\_type|
|Compute Security Group|cmdb\_ci\_compute\_security\_group|
|Image|cmdb\_ci\_os\_template|
|Cloud Image|cmdb\_ci\_cloud\_os\_image|
|Cloud Load Balancer|cmdb\_ci\_cloud\_load\_balancer|
|Cloud Resource|cmdb\_ci\_cmp\_resource|
|Cloud File Service|cmdb\_ci\_cloud\_file\_service|
|Cloud Mgmt Network Interface|cmdb\_ci\_nic|
|Endpoint|cmdb\_ci\_endpoint|
|Cloud Function|cmdb\_ci\_cloud\_function|
|Cloud Object Storage|cmdb\_ci\_cloud\_object\_storage|
|Cloud Gateway|cmdb\_ci\_cloud\_gateway|
|Database Instance|cmdb\_ci\_db\_instance|
|Cloud DataBase|cmdb\_ci\_cloud\_database|
|DynamoDB Table|cmdb\_ci\_dynamodb\_table|

## Supported virtual machine tables

The following virtual machine tables are referenced in the Virtual Machine Object \[cmdb\_ci\_vm\_object\] field in the Hardware table:

|Table label|Table name|
|-----------|----------|
|Windows Server|cmdb\_ci\_win\_server|
|Linux Server|cmdb\_ci\_linux\_server|

-   **[Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md)**  
Populate Service Account, Logical Datacenter, and Virtual Machine Object fields in configuration item \(CI\) tables to improve query performance.
-   **[Set the Populate Service Account and LDC job stale threshold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-stale-days.md)**  
Configure the number of days before a running **Populate Service Account and LDC IN CMDB** job is considered stale and canceled. Increase this value if a large configuration item \(CI\) dataset causes the job to be canceled before a full run completes.
-   **[Trigger a full CI table resync for direct field population](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-full-resync.md)**  
Trigger the **Populate Service Account and LDC IN CMDB** scheduled job to reprocess all configuration item \(CI\) records. Configure the **sn\_itom\_pattern.populate\_saldc\_full\_resync** system property when service accounts or logical datacenters have incorrect or corrupted values for a CI.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md)

**Previous topic:**[Discover datacenters only for new cloud accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/discover-datacenter-only-new-account.md)

**Next topic:**[Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md)

**Related topics**  


[Available cloud discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns-cloud.md)

[Linux discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoLinuxComputers.md)

[Windows discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoWindowsComputers.md)

