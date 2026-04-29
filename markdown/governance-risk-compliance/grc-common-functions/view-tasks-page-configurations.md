---
title: Update the Tasks Page Configuration record
description: Update the Tasks Page Configuration record in the classic user interface to display the task configurations in various workspaces. The Tasks Page Configuration record displays the configurations that an end user can view in the My Tasks landing page in each workspace.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Landing Page Configurations module, Common GRC features, Governance, Risk, and Compliance]
---

# Update the Tasks Page Configuration record

Update the Tasks Page Configuration record in the classic user interface to display the task configurations in various workspaces. The Tasks Page Configuration record displays the configurations that an end user can view in the My Tasks landing page in each workspace.

## Before you begin

Role required: sn\_grc.admin, sn\_grc\_workspace.task\_admin

## About this task

GRC administrators can configure the tasks that the workspace users can view in the workspace. The following tabs are used to configure the tasks and they are provided by default for each workspace:

-   My pending tasks
-   My group's tasks
-   My items
-   Watchlist

Depending on the workspace selection, these configurable tabs are displayed in the workspace. GRC administrators can modify these tabs using the Landing Page Configurations module.

State filters or second-level filters are available for the My pending tasks, My group's tasks, My items, and Watchlist tabs.

## Procedure

1.  Navigate to **All** &gt; **GRC Landing Page Configurations** &gt; **Tasks Page Configuration**.

    The Tasks Page Configuration record displays the configuration records for each of the following workspaces:

    -   Audit Workspace
    -   Compliance Workspace: Displayed under the Policy and Compliance module.
    -   Operational Resilience workspace
    -   Privacy Workspace
    -   Regulatory Change Management Workspace: Displayed under the Policy and Compliance module.
    -   Risk Workspace
    -   Risk Portal
    -   Vendor Management Workspace
2.  Click the configuration record for the workspace that you are working in.

3.  On the form, update the fields as needed.

    The tasks page configuration record for the selected workspace displays the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the task configuration that is displayed in the tasks page configuration record.|
    |Description|Description of the task configuration that can be updated.|
    |Workspace title|Title of the My Tasks page that is displayed in the workspace.|

    The **Tab Configurations** related list displays the following tabs in the Task Configuration record:

    -   My pending tasks
    -   My group's tasks
    -   My items
    -   Watchlist
    -   Confidential records
    The following configuration fields are displayed for all the tabs in the Task Configuration record:

    |Field|Description|
    |-----|-----------|
    |Tab name|Name of the tab that is displayed in the workspace.|
    |Order|Order of the tab in the workspace.|
    |Display tab|Option to display the tab in the UI. When this option is enabled, the tab is displayed in the UI. Similarly, when this option is disabled, the tab is not displayed in the UI.|
    |Enable group selection|Option to select the groups in the filter. When this option is enabled, administrators can filter the records based on the group selection for the applicable table.|

    The related list for each tab displays the following information:

<table id="table_lph_qhd_tqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applicable tables

</td><td>

List of the tables that are displayed in the workspace and that are shipped with the release. These tables are the records that the user can act upon based on the matching conditions.

 You can create a new applicable table or click an existing applicable table from the list to update its configuration record.

 -   The table configuration record displays the fields that are related to the selected applicable table.
-   The Map states related list displays the states that are applicable to the selected applicable table. You can select a state and update its filter condition so that it is correctly displayed in the tab in the workspace.


</td></tr><tr><td>

Applicable states

</td><td>

List of the states that are applicable to the tab. These states are displayed in the workspace with the Overridden label column. You can configure and update the name of the state by adding the updated state name in the Overridden label column.

</td></tr></tbody>
</table>4.  If needed, in the Applicable tables related list, update an existing table by doing the following:

    1.  Click a table to open its configuration record.

    2.  Configure the **Task title**, **Table**, **Tab level filter**, and **Displayed columns** fields and click **Update**.

        The updated fields for the selected table are displayed to the end user in the workspace.

    3.  Configure the name of the state by adding the updated state name in the Overridden label column.

5.  Click the **My pending tasks** tab and update the configuration fields if necessary.

    The My pending tasks tab configuration displays the available configuration and the list of the tasks configured within the tab.

6.  Click the **My group's tasks** tab and update the configuration fields if necessary.

    The My group's tasks tab configuration displays the list of the tasks assigned to your group.

    **Note:** You can configure the tab name for the My group's tasks tab and its associated fields similar to the My pending tasks tab.

7.  Click the **My items** tab and update the fields if necessary.

    The My items tab configuration displays the list of items that are either created by you or opened by you.

    **Note:** You can configure the tab name for the My items tab and its associated fields similar to the My pending tasks tab.

8.  Click **Watchlist** and update the fields if necessary.

    The My watchlist tab configuration displays the list of the tasks for which you are in the watchlist.

    **Note:** You can configure the tab name for the Watchlist tab and its associated fields similar to the My pending tasks tab.

9.  Click **Confidential records** and update the configuration fields if necessary.

    The Confidential records tab configuration displays the confidential records for the selected table.

10. Click **New** in the **Tab Configurations** related list to add a new tab in the Task Configuration record.

    1.  Fill in the fields on the form.

    2.  Click **Submit**.

    The new tab is displayed in the UI with the information for the selected groups.

11. Click **Update** to update the task configuration record.


**Parent Topic:**[Landing Page Configurations module](../reference/admin-config-using-grc-common.md)

