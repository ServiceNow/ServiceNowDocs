---
title: Delete CIs
description: You can use the CI Class Manager to delete CIs that are no longer needed.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Delete CIs

You can use the CI Class Manager to delete CIs that are no longer needed.

## Before you begin

Role required: sn\_cmdb\_admin or itil\_admin

## About this task

For information about policy-based, large scale automated CI deletions, see [Working with CMDB Data Manager](../concept/cmdb-data-management.md).

**Note:** You can't delete base system tables. For information about deleting custom tables, see Deleting custom tables.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Click **Hierarchy** to expand the CI Classes list and then select the class from which you want to delete CI records.

3.  In the class navigation bar on the left, click **CI List**.

4.  On the CI List form view, select the CIs that you want to delete.

    Select the check box in the header to select all the CIs that are visible.

5.  Click **Actions on selected rows** and then click **Delete**.

6.  Click **Delete** in the **Confirmation** dialog box.


## Result

After deleting CIs that a dependent CI depends on, the dependent relationship is also deleted. The dependent CI becomes an orphan and is not immediately deleted. In this situation, the system attempts to cascade delete such orphan dependent CIs to prevent the accumulation of stale data and maintain the health of the CMDB. For information about how the system manages orphan dependent CIs, see [Management of orphan dependent CIs](../concept/c_CMDBClassifications.md).

**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](t_CreateCIType.md)

[Reclassify a CI](t_ManuallyReclassifyCI.md)

[View and edit class definitions and metadata](t_ViewTableDefinitions.md)

[Update the list of classes in the Principal Class filter](update-principal-class-filter.md)

