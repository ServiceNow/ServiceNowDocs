---
title: Manage exclusion lists of CMDB Data Manager \(in Core UI\)
description: Create an exclusion list for the various policy types of the CMDB Data Manager, by using the CMDB Data Manager legacy build on Core UI. Policies of a specific policy type will not target the CIs or other records in the exclusion list for that policy type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/manage-data-mgr-ci-exclusion-list.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CMDB Data Manager \(Core UI\), CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage exclusion lists of CMDB Data Manager \(in Core UI\)

Create an exclusion list for the various policy types of the CMDB Data Manager, by using the CMDB Data Manager legacy build on Core UI. Policies of a specific policy type will not target the CIs or other records in the exclusion list for that policy type.

## Before you begin

Role required:

-   data\_manager\_admin: Full access to CI exclusion lists
-   data\_manager\_user: Read access and can add a CI to a CI exclusion list

## About this task

**Note:** Regardless of where you manage exclusion lists, the list is used in both the Data Manager \(Core UI\) and Data Manager in CMDB Workspace. For information about managing CI exclusion lists in the more advanced CMDB Data Manager in CMDB Workspace, see [CMDB Data Manager experience in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/data-mgr-exp-cmdb-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Data Manager**.

2.  On the CMDB Data Manager landing page, in the Excluded CIs tile, click **View Excluded CIs**.

3.  On the Excluded CIs list view, click **Edit Exclusion List** and fill out the Specify Excluded CIs form.

    |Field|Description|
    |-----|-----------|
    |Policy Type|Type of policy from which to exclude the specified CIs.|
    |Condition Filter|Conditions that CIs must meet to be excluded for the specified policy type.|

4.  Click **Run filter**.

    All the CIs that meet the condition filters, appear in the Results section.

5.  In the Results list, select any or all of the CIs that you want to exclude from the policies of the respective policy type.

6.  In the Excluded CIs section, click the '+' icon to add the selected CIs to the Excluded CIs list.

7.  In the Excluded CIs list, select CIs that you want to remove from the exclusion list, then click the trash icon.

8.  Click **Save**.


