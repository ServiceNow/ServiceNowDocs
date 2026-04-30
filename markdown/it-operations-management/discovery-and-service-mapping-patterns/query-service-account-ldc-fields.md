---
title: Improved query performance with direct field population in CI tables
description: The Populate Service Account and LDC IN CMDB scheduled job populates the Service Account and Logical Datacenter fields in cloud configuration item \(CI\) tables, and the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. This direct population reduces query complexity and improves query performance.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 3
keywords: [cloud CI tables, Service Account, Logical Datacenter, query performance, cloud discovery]
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Improved query performance with direct field population in CI tables

The **Populate Service Account and LDC IN CMDB** scheduled job populates the Service Account and Logical Datacenter fields in cloud configuration item \(CI\) tables, and the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. This direct population reduces query complexity and improves query performance.

Cloud Service Account \(such as AWS Account, Azure Subscription, or GCP Project\) and Logical Datacenter \(such as AWS, Azure, or GCP Regions\) information is stored separately from cloud CIs. To retrieve account or datacenter information for a cloud resource, queries require joins across multiple tables, including the relationship table that connects CIs. Similarly, Virtual Machine Object information is stored separately from the Hardware CI, requiring additional joins to retrieve data from the Virtual Machine Object \[cmdb\_ci\_vm\_object\] table. With potentially millions of records in the relationship table, these joins could increase query time for teams working with cloud infrastructure data.

Starting with the Discovery and Service Mapping Patterns version 1.30.2, you can enable a feature that denormalizes cloud CI tables by populating the **Service Account** \[cloud\_service\_account\] and **Logical Datacenter** \[logical\_datacenter\] fields directly in cloud CI tables. The scheduled job also references tables extended from the Virtual Machine Object \[cmdb\_ci\_vm\_object\] table via the Virtual Machine Object reference field in the Hardware \[cmdb\_ci\_hardware\] table. Populating these fields directly reduces the need for complex joins, supporting more efficient queries for reporting, analytics, and operational workflows involving cloud resources. After you enable this feature, Discovery populates these fields for both existing and newly discovered CIs.

![Comparison between complex multi-table joins without the feature versus direct field access with the feature](../image/multi-joins-vs-direct-fields.png "Query process with and without field population")

For information about enabling this feature, see [Enable direct field population for query performance](../task/populate-service-account-ldc-fields.md).

## Supported Cloud CI tables

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

-   **[Enable direct field population for query performance](../task/populate-service-account-ldc-fields.md)**  
Populate Service Account, Logical Datacenter, and Virtual Machine Object fields in configuration item \(CI\) tables to improve query performance.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](c_MappingPatternsCustomization.md)

**Previous topic:**[Discover datacenters only for new cloud accounts](../task/discover-datacenter-only-new-account.md)

**Next topic:**[Enable direct field population for query performance](../task/populate-service-account-ldc-fields.md)

**Related topics**  


[Available cloud discovery patterns](available-patterns-cloud.md)

[Linux discovery](../../discovery/reference/r_DataCollDiscoLinuxComputers.md)

[Windows discovery](../../discovery/reference/r_DataCollDiscoWindowsComputers.md)

