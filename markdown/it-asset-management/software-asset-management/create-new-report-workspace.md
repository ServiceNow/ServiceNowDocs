---
title: Create and manage reports in workspace
description: Create and manage your report tiles in the Software Asset Workspace.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create and manage reports in workspace

Create and manage your report tiles in the Software Asset Workspace.

## Before you begin

Role required: sam\_admin or admin

## About this task

All the base system Software Asset Management reports and the custom created reports are stored in the SAM Workbench Report \[samp\_workbench\_report\] table. List reports are supported by default. For creating other types of reports, you need to create a UIB page in the Software Asset Workspace with the necessary data visualization. A parameter called **reportSysId** needs to be passed to the UIB page. You can use the UIB page's route in the report tile creation form after it has been built.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License usage**.

2.  In the License usage view, select the **Reports** tab.

    ![Reports tab](../image/reportstab-workspace.png)

3.  Select **Manage Reports**.

4.  In the Reports list view page, select **New**.

    ![Create a new report](../image/create-report-workspace.png "Create New SAM Workbench Report form")

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Title|The title of the report tile.|
    |Description|A brief description of the report tile.|
    |Type|The type of the report. For example, list, bar, pie chart. The default value is List.|
    |Icon|The unique icon identifier from the Now Design System icon library. Examples include chart-bar-group-fill, chart-pie-fill. The default value is list-fill.|
    |Route|This the path taken by a report when it is clicked. This takes you to the list view of the source table with the specified filter conditions. This can be routed to any other page within the Software Asset Management application provided that the page accepts the **reportSysId** parameter. The default value is list-report.|
    |Source table|The table on which the report is based.|
    |Filter \(Set conditions\)|The filter to be used on the list report.|

6.  Select **Save**.

    The new report tile appears on the Reports tab. You may need to reload the Reports tab to see the new report tile.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

