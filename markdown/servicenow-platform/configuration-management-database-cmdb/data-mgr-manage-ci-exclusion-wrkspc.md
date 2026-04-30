---
title: Manage exclusion lists for CMDB Data Manager
description: Create and manage exclusion lists for the various policy types used in CMDB Data Manager, in CMDB Workspace or in Service Graph Workspace. Policies of the specified type won't target CIs and other records in the exclusion list for that policy type.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer CMDB Data Manager, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage exclusion lists for CMDB Data Manager

Create and manage exclusion lists for the various policy types used in CMDB Data Manager, in CMDB Workspaceor in Service Graph Workspace. Policies of the specified type won't target CIs and other records in the exclusion list for that policy type.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

**Note:** The Certification policy type doesn't support exclusion lists.

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then select the **Data Manager** quick link on the Home view.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Governance icon. Then, in the Governance pane, select **Data Manager overview**.
2.  Select **Excluded records** in the left-side bar.

    The Excluded records list view shows lists of all records currently excluded, grouped by policy type. You can expand any group to show its CIs and other records and then drill down to any record.

3.  Remove excluded records from the exclusion list:

    1.  Expand a policy type group to show its list of excluded records.

    2.  In the list view, select the records that you want to remove from the exclusion list.

    3.  Select **Remove from list**

    4.  In the Confirm removal from exclusion list dialog box, select **Confirm**.

    The selected records are removed from the exclusion list and can be targeted for the policy type.

4.  Add records to an exclusion list:

    1.  Select **Exclude Records** and fill out the Data Filter form.

        |Field|Description|
        |-----|-----------|
        |Tables|Table from which to select CIs or records for the exclusion list.|
        |Filter conditions|Use the condition builder to specify the criteria that CIs or records from the specified **Tables** must meet to be included in the exclusion list.|
        |Related List Condition|Add a condition that is based on related lists that are associated with the records that you want to exclude.|

    2.  Select **Apply filters** and then review the Search results list.

    3.  Select the records that you want to add to exclusion lists and then select **Continue**.

    4.  On the Select policy type page, select the policy types for which to exclude the selected records and then select **Continue**.

    5.  Review the details of the exclusion on the summary page and then select **Save**.


