---
title: Convert legacy certification schedules into Data Manager certification policies in CMDB Workspace or in Service Graph Workspace
description: Convert certification schedules created in the legacy Data Certification application \(running on Core UI\), into draft Data Manager certification policies available in CMDB Workspace or in Service Graph Workspace.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Convert legacy certification schedules into Data Manager certification policies in CMDB Workspaceor in Service Graph Workspace

Convert certification schedules created in the legacy Data Certification application \(running on Core UI\), into draft Data Manager certification policies available in CMDB Workspaceor in Service Graph Workspace.

## Before you begin

Role required: data\_manager\_admin or sn\_cmdb\_admin

## About this task

If you have been using the legacy Data Certification application on Core UI, then any associated certification schedules might not be automatically available in the implementation of Data Certification in CMDB Workspace and in Service Graph Workspace. You can convert those definitions into draft Data Manager Certification policies. Then you can publish those converted policies in CMDB Workspaceor in Service Graph Workspace just like publishing any draft Data Manager policy.

Important things to know:

-   Legacy certification schedules that were successfully converted are automatically deactivated.
-   This conversion migrates most fields from the legacy certification schedule. However, the **Assign to empty** and the **Last run date** fields aren't migrated into CMDB Workspace and Service Graph Workspace Data Manager tables.
-   Any dot-walking settings in the legacy certification schedules used for assignments of **User Field** or **User Group Field** are preserved in this conversion.

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and select **Management** in the CMDB Workspace menu bar. Then, select the **Data Manager** link in Management tools, in the Manage section.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel, select the Governance icon. Then, in the Governance navigation pane, select **Data Manager overview**.
2.  On the Data Manager overview page, select **Import** on the banner at the top of the page.

    If there aren't any legacy certification schedules to import, the notification banner about importing existing policies doesn't appear.

3.  In the Confirm import of certification schedule into draft policies, select **Import into draft policies**.

    1.  Track progression in the Import in progress dialog box.

    2.  Review the import results in the Import summary dialog box.

        If there were earlier conversion operations, the results reflect only the current conversion operation. For example, the Completed count includes only those records that were successfully converted in the current run.

        Select the links associated with the completed and skipped results to drill down to the associated records.

        Also, to see additional details, select **All** and in the Filter navigator, enter `cert_schedule.list` to open the Certification Schedules table. The **Migration Status** and the **Migration exception** columns provide details that are especially important for failed and skipped records.

    3.  Select **View draft policies** to view the converted policies in the Data Manager policies page, under the Draft policies tab.

4.  [Publish a draft CMDB Data Manager policy](data-manager-publish-draft-policy.md)


## Result

-   If you log in while this conversion is in process, a progress message appears on the Data Manager overview page. You can select the **View details** link to open the Import in progress dialog box with details about the progress of the operation.
-   The legacy certification schedules are available as draft Certification policies in Data Manager in CMDB Workspace and in Service Graph Workspace.
-   The legacy certification schedules are deactivated.
-   The legacy certification tasks are unchanged and you can review and resolve them as needed.

