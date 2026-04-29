---
title: Recompute CI attribute values
description: Modify reconciliation rules, or exclude a discovery source which is found to be invalid. Then, use the updated reconciliation rules in recomputing CI attribute values, for which those reconciliation rules or discovery source are applicable to.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CMDB 360, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Recompute CI attribute values

Modify reconciliation rules, or exclude a discovery source which is found to be invalid. Then, use the updated reconciliation rules in recomputing CI attribute values, for which those reconciliation rules or discovery source are applicable to.

## Before you begin

[Enable and configure CMDB 360](../concept/multisource-cmdb.md#section_enable_multisource_CMDB).

If you want to recompute to apply updated reconciliation rules, then you must first update the reconciliation rules.

Role required: sn\_cmdb\_admin or itil\_admin

## About this task

CMDB 360 automatically generates a recompute task for each recompute that you submit. If you submit multiple recomputes, a recompute task is generated for each operation, but only one task runs at any given time. To list all recompute tasks, enter `cmdb_multisource_recomp_task.list` in the left navigation search box.

There is a maximum number of records that can be included in a single recompute operation. This number is specified by the system property [glide.identification\_engine.multisource.recompute.max.ci.limit](../reference/components-multisource-cmdb.md) \(100,000 by default\).

**Note:**

-   Recompute skips CIs which are reported by multiple discovery sources, but with different class names.
-   Recomputing CI attribute values is not supported with non-CMDB tables.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select a class from the CI Classes hierarchy list.

3.  In the left-side pane, expand **Class Info**, and select **Reconciliation Rules**.

4.  On the Reconciliation Rules page, click **Recompute**.

5.  Select the **Recompute Type**.

    -   **Replace values from the specified discovery source with value from the discovery source next in priority, according to reconciliation rules**: Recompute attribute values for the class CIs, applying priorities specified in reconciliation rules and while excluding the specified **Discovery Source**. Records for the discovery source you are excluding, are also removed from the CMDB 360 data store.

        This operation applies to data that exists in the CMDB. If reconciliation rules remain in effect for the discovery source that you have excluded, then future data from that discovery source, can populate the CMDB.

    -   **Apply updated reconciliation rules**: Recompute attribute values for the class CIs, applying the updated reconciliation rules which are now in effect.
6.  Select the **Recompute Scope**.

    The scopes grow from one option to the next:

    -   **Recompute only CIs of this class**: Basic scope of CIs to recompute.
    -   **Recompute CIs of this and derived classes**: Expand the basic scope to include CIs from derived classes.
    -   **Recompute CIs of this and derived classes, along with selected related items**: Expand the previous scope to also include CIs from specified related items. Select the related items to include in the recompute.
7.  Select the **Delete action** for CIs for which the excluded discovery source, is the only discovery source.

    -   **Delete record**: Delete the CI record from CMDB.
    -   **Set record attributes to custom value**: Set a specified CI attribute to a custom value to remove the CI from regular operations without deleting the CI. For example, set the **Operational status** attribute to **Retired**.
8.  Select **Next**.

9.  On the Review page, carefully review the counts for the affected CIs to ensure that all record counts are as you expect.

10. Select **Back** to adjust any settings for the recompute.

11. Select **Recompute**.


## What to do next

You can do any of the followings:

-   In the status message that appears for the recompute operation, click the link to see the CMDB 360 Recompute Task for more details. The Recompute Task shows the progress and status of the recompute operation.

    You can abort the recompute by setting **Status** to **Closed Incomplete** and selecting **Update**. You can then set **Status** back to **Work in progress** to resume recompute from where it was aborted.

-   Enter `cmdb_multisource_recomp_task.list` in the left navigation search box, to see the status and progress of all recompute tasks.

