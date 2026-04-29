---
title: IRE support for non-CMDB tables
description: Apply Identification and Reconciliation Engine \(IRE\) processes to supported non-CMDB tables to ensure data integrity and health of those tables.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# IRE support for non-CMDB tables

Apply Identification and Reconciliation Engine \(IRE\) processes to supported non-CMDB tables to ensure data integrity and health of those tables.

Starting with the Australia release, IRE supports some non-CMDB tables. You can use all IRE features with some non-CMDB tables after creating identification rules \(CI identifiers and identifier entries\) for those tables. Non-CMDB tables supported for IRE features include:

-   In an application-specific scope: All non-CMDB tables
-   In the global scope: Only non-CMDB tables that are preset in the base system. In the Australia release for example, the Location \[cmn\_location\], Department \[cmn\_department\], Cost Center \[cmn\_cost\_center\], Building \[cmn\_building\], User \[sys\_user\], and Group \[sys\_user\_group\] non-CMDB tables are supported.

You can't use the [CI Class Manager](../reference/ci-class-manager-landing-page.md) to manage any IRE-related rules for non-CMDB tables. Instead, you must work directly with the respective tables in list views to create and manage those rules as described in the following procedures:

-   [Create an identification rule for a non-CMDB table](../task/create-non-cmdb-id-rule.md)
-   [Create a reconciliation rule for a non-CMDB table](create-reconciliation-rule-non-cmdb.md#)
-   [Create an IRE data source rule for non-CMDB tables](../task/create-non-cmdb-ire-data-src-rule.md)
-   [Create a data refresh rule for a non-CMDB table](../task/create-non-cmdb-data-refresh-rule.md)
-   [Create an identification inclusion rule for a non-CMDB table](../task/create-non-cmdb-id-inclusion-rule.md)
-   [Simulate payload execution using identification simulation](identification-simulation.md#)
-   [Use partial payloads](ire.md)
-   [Review and process de-duplication tasks](de-duplication-tasks.md)

You can use the following store apps with supported non-CMDB tables:

-   [CMDB 360 in CMDB Workspace](cmdb-workspace-cmdb360-view.md)
-   [IntegrationHub ETL](integrationhub-etl.md)

IRE processes are applied to supported non-CMDB tables with the following differences:

-   IRE doesn't populate the **discovery\_source**, **last\_discovered**, and the **first\_discovered** attributes if those attributes don't exist in the non-CMDB table.
-   IRE uses the non-CMDB table’s class name as **sys\_class\_name** if the table doesn't include a **sys\_class\_name** attribute.
-   IRE payloads don't support relationships with non-CMDB tables.

**Note:** Although IRE-related user interface and accompanying documentation might reference CMDB and CMDB elements, most of those references also apply to any supported non-CMDB tables.

-   **[Create an identification rule for a non-CMDB table](../task/create-non-cmdb-id-rule.md)**  
To use Identification and Reconciliation Engine \(IRE\) features with supported non-CMDB tables, you must first create identification rules that uniquely identify the table records. Each non-CMDB table can be associated with a single identification rule.
-   **[Create a reconciliation rule for a non-CMDB table](create-reconciliation-rule-non-cmdb.md#)**  
Create a static or a dynamic CI reconciliation rule for a non-CMDB table.
-   **[Create a data refresh rule for a non-CMDB table](../task/create-non-cmdb-data-refresh-rule.md)**  
To apply Identification and Reconciliation Engine \(IRE\) features to supported non-CMDB tables, create data refresh rules for those tables. Data refresh rules are used to determine if a record is stale for a specific data source. Such records can then be updated by a lower-priority authorized data source.
-   **[Create an identification inclusion rule for a non-CMDB table](../task/create-non-cmdb-id-inclusion-rule.md)**  
Narrow the scope of records that are included in the identification process of non-CMDB records by creating an identification inclusion rule.
-   **[Create an IRE data source rule for non-CMDB tables](../task/create-non-cmdb-ire-data-src-rule.md)**  
When using Identification and Reconciliation Engine \(IRE\), you can prevent a specific data source from inserting new records for a specific non-CMDB table. Create IRE data source rules for data sources that you don't trust in creating records but continue to trust in updating those records that exist.

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md)

