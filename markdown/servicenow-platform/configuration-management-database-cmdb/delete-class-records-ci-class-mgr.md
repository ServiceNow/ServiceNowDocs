---
title: Delete CIs
description: You can use the CI Class Manager to delete CIs that are no longer needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/delete-class-records-ci-class-mgr.html
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

For information about policy-based, large scale automated CI deletions, see [Working with CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.md).

**Note:** You can't delete base system tables. For information about deleting custom tables, see [Deleting custom tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DeleteATable.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Click **Hierarchy** to expand the CI Classes list and then select the class from which you want to delete CI records.

3.  In the class navigation bar on the left, click **CI List**.

4.  On the CI List form view, select the CIs that you want to delete.

    Select the check box in the header to select all the CIs that are visible.

5.  Click **Actions on selected rows** and then click **Delete**.

6.  Click **Delete** in the **Confirmation** dialog box.


## Result

After deleting CIs that a dependent CI depends on, the dependent relationship is also deleted. The dependent CI becomes an orphan and is not immediately deleted. In this situation, the system attempts to cascade delete such orphan dependent CIs to prevent the accumulation of stale data and maintain the health of the CMDB. For information about how the system manages orphan dependent CIs, see [Management of orphan dependent CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CMDBClassifications.md).

**Parent Topic:**[CMDB classifications and class dependency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management]()

[CMDB record types]()

[Related Lists of CI components]()

[Create a CI class]()

[Reclassify a CI]()

[View and edit class definitions and metadata]()

[Update the list of classes in the Principal Class filter]()

