---
title: CMDB 360
description: CMDB 360 retains complete history about discovery sources and proposed values, involved in updates of CI attributes. Use CMDB 360 data to track how the CMDB is populated by various discovery sources at the CI attribute level. Also, to revert CI updates from a specific discovery source, or to recompute attribute values using updated reconciliation rules.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB 360

CMDB 360 retains complete history about discovery sources and proposed values, involved in updates of CI attributes. Use CMDB 360 data to track how the CMDB is populated by various discovery sources at the CI attribute level. Also, to revert CI updates from a specific discovery source, or to recompute attribute values using updated reconciliation rules.

CMDB 360 provides all the functionality of the legacy Multisource CMDB feature with additional capabilities such as an analytics dashboard, and new query functionality. You can access all of the CMDB 360 capabilities in the [CMDB 360 view in CMDB Workspace](cmdb360-exp-cmdb-workspace.md)or in the [CMDB 360 insights dashboard in Service Graph Workspace](sg-workspace-insights-cmdb360.md).

## How CMDB 360 works

When multiple discovery sources attempt to update the same CI attribute, the [Identification and Reconciliation Engine \(IRE\)](c_CMDBIdentifyandReconcile.md) uses reconciliation rules to select a single discovery source for the update. Without CMDB 360, details about the lower-priority discovery sources whose values were rejected, are discarded. Also, it is difficult to identify the source of an attribute value without CMDB 360.

With CMDB 360, the raw details for every discovery source and CI combination are retained for both, discovery sources that were selected for an update and all others that were not. CMDB 360 data, consisting of records for each discovery source and CI combination, is stored in the CMDB MultiSource Data \[cmdb\_multisource\_data\] table. You can examine, query, and report on the CMDB 360 data store.

You can optionally exclude classes and their descendents from collecting and processing CMDB 360 data. The CMDB MultiSource Data \[cmdb\_multisource\_data\] table doesn't contain data for those excluded classes. For more information, see [Exclude classes from CMDB 360](../task/exclude-class-cmdb360.md).

**Note:** CMDB 360 supports non-CMDB tables. The widely used term Configuration Item \(CI\), can also refer to a non-CMDB table record. For information about support for non-CMDB tables, see [IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md).

![Data flow from initial ingestion and refinement before it is stored in the CMDB, and the type of insights that CMDB 360 provides into these processes.](../image/MultisourceCMDB.png "CMDB 360 insights into data source processes")

After data is initially ingested from multiple data sources, several processes are applied to standardize and reconcile the data before it is stored in the CMDB. CMDB 360 provides insights that can help you configure some of these processes.

## Using CMDB 360

Use CMDB 360 to:

-   [Create a dynamic reconciliation rule](create-reconciliation-rule.md#).
-   Control CI updates at the discovery source and CI attribute level.
-   Visualize discovery sources of attribute values, at the attribute level.
-   Modify reconciliation rules and then recompute CMDB data, reflecting the updated reconciliation rules.
-   Revert CMDB data integration from a specific discovery source, if, for example, you realize that the discovery source is not reliable. Recompute CI attribute values, while excluding the discovery source that you want to ignore.
-   Validate a new discovery source by comparing its data to data from other discovery sources, which are known to be valid.
-   Improve data management, data quality, and operational insights, by querying on CMDB 360 data. Use the CMDB 360 query builder in CMDB Workspaceor in Service Graph Workspace to create queries for CMDB 360 records, discovery sources, and CI records.

## Enable and configure CMDB 360

-   [Activate](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US) the ITOM Discovery License \(com.snc.itom.discovery.license\) plugin.
-   Navigate to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**. Then, in the CMDB 360 Properties pane ensure that the [glide.identification\_engine.multisource\_enabled](../reference/components-multisource-cmdb.md) \(Enables CMDB 360\) property is set to **true**.
-   Optionally, [Exclude classes from CMDB 360](../task/exclude-class-cmdb360.md).

By default, CMDB 360 tracks discovery source information for CIs from CMDB classes and doesn't collect data for non-CMDB tables. You can independently enable or disable tracking data for CMDB and for non-CMDB classes, using these system properties: ​

-   [glide.identification\_engine.multisource\_cmdb\_ci\_enabled](../reference/components-multisource-cmdb.md) \(Enables capturing CMDB 360 data for CIs from CMDB classes\)​
-   [glide.identification\_engine.multisource\_non\_cmdb\_ci\_enabled](../reference/components-multisource-cmdb.md) \(Enables capturing CMDB 360 data for CIs from non-CMDB classes\)

## Report on CMDB 360 data

Use the [CMDB 360 view in CMDB Workspace](cmdb-workspace-cmdb360-view.md)or [CMDB 360 insights dashboard in Service Graph Workspace](sg-workspace-insights-cmdb360.md) to gain insights into the CMDB 360 data store. Build reports that, for example, do the followings:

-   Find CIs not reported by any discovery source.
-   Find discovery sources populating data in your CMDB.
-   Compare attribute values across discovery sources.
-   Compare attribute values between CMDB and other discovery source.
-   Limit reports for CMDB 360 data, to a specific application service, technical service, or a CMDB group.

## Visualize CMDB 360 data

CMDB 360 is highly verbose in the user interface:

-   On the [Reconcliation Rules](create-reconciliation-rule.md#) page in CI Class Manager, click the **Preview Data** tab to see per attribute, discovery sources that are authorized to update that attribute, in precedence order.
-   On a CI form, click the **CMDB 360 Data Preview** related link to see per CI attribute, current value in the CMDB and incoming values from other discovery sources.

## Logging

Enable logging for CMDB 360 by adding and enabling the system property ​ [glide.cmdb.logger.source.cmdb\_multisource](../reference/components-multisource-cmdb.md). In the Log \[syslog\] table, search for entries in which `source=“cmdb_multisource”`.

