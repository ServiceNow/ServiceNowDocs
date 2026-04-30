---
title: Configuration Item \[cmdb\_ci\] class
description: Attributes in the Configuration Item \[cmdb\_ci\] class, which extends the Base Configuration Item \[cmdb\] class.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CMDB schema model, Explore, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuration Item \[cmdb\_ci\] class

Attributes in the Configuration Item \[cmdb\_ci\] class, which extends the Base Configuration Item \[cmdb\] class.

**Warning:** Do not modify any of these attributes in the dictionary. For example, do not modify the type of the **location** attribute from reference to list. Such modifications may prevent features that use the CMDB, from functioning properly.

For descriptions of common CMDB tables in a base system, see [CMDB tables descriptions](cmdb-tables-details.md).

## Common core, user tables

![Common core, user tables.](../image/CriticalCommonCoreUserTables.png)

## CMDB CI schema related to common core and non-core tables

![CMDB CI schema related to common core and other tables.](../image/CISchemaModel.png)

## Attributes

|Attribute|Description|
|---------|-----------|
|Asset tag|Asset tag/service tag for the specific asset|
|Assigned|Date and time of assignment to user|
|Attributes|Description of usage of attributes for the instance|
|Can Print|Indicates whether the instance can print|
|Category|Name of category applicable to the instance|
|Checked in|Date and time of checking in|
|Checked out|Date and time of checking out|
|Class|System class name|
|Comments|Comments related to the instance|
|Correlation ID|ID of the instance from another data source|
|Cost|Financial value in local currency \(as defined in the Cost Currency field\)|
|Cost currency|Name of currency \(such as dollars, pounds, Euros\)|
|Created|Date and time record was created|
|Created by|Name of person/data source which initially created the record|
|Description|Fit \(how deployed\) and function \(purpose\) of the instance|
|Discovery source|Name of primary \(most trusted\) discovery source|
|DNS Domain|Name of the DNS domain to which the instance belongs|
|Domain|ID of the domain to which the instance belongs|
|Domain Path|Path of the domain to which the instance belongs|
|Due|Date and time instance was due|
|Due in|Description of the manner of which the instance was due|
|Fault Count|Number of faulty recorded against the instance to date|
|First Discovered|Date and time instance was initially discovered|
|Fully Qualified Domain Name|Full path name of domain to which the instance belongs|
|GL account|General Ledger account name/number|
|Installed|Date and time instance was most recently installed|
|Invoice number|Invoice number used in acquisition process|
|IP Address|Primary IP address used by the instance|
|Justification|Description of the justification for the instance|
|Lease contract|Number of current leasing contracts|
|MAC Address|MAC address of the instance|
|Model Number|Manufacturer original model number|
|Monitor|Indicates whether the instance is monitored|
|Most Recent Discovery|Date and time instance was last discovered|
|Name|Name of the CI instance|
|Operational Status|Configurable choice list with values for current operational states|
|Order received|Date and time instance was initially received|
|Ordered|Date and time instance was initially ordered|
|PO number|Purchase order number used in acquisition process|
|Purchased|Date instance was purchased|
|Requires verification|Flag indicating whether verification is required for the instance|
|Serial number|Serial number of the instance|
|Skip sync|Flag indicating whether synchronization between Asset Management and CMDB can be skipped|
|Start Date|Date and time the instance was last started|
|Subcategory|Name of Subcategory applicable to the instance|
|Sys ID|ServiceNow Sys ID \(GUID\)|
|Tags|Related tags|
|Updated|Date and time instance was last updated|
|Updated by|Person/data source which last updated the record|
|Updates|Configurable choice list with values for update states|
|Warranty expiration|Date current warranty expires|

|Reference attribute|Reference to|
|-------------------|------------|
|Approval Group|Group table|
|Asset|Asset table|
|Assigned to|User table|
|Change Group|Group table|
|Company|Company table|
|Cost center|Cost Center table|
|Department|Department table|
|Location|Location table|
|Maintenance Schedule|Schedule table|
|Managed by|User table|
|Manufacturer|Company table|
|Model ID|Product Model table|
|Owned by|User table|
|Schedule|Schedule table \(for normal processing\)|
|Support group|Group table|
|Supported by|User|
|Vendor|Company table|

