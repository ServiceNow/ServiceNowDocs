---
title: Add or modify Express List columns
description: Add columns to the Event Management Express List display to focus the list of alerts that is displayed or modify the existing columns that are displayed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/service-operations-workspace-for-itom-apps/edit-list-columns-el.html
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Add or modify Express List columns

Add columns to the Event Management Express List display to focus the list of alerts that is displayed or modify the existing columns that are displayed.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express List icon \(\[Omitted image "express-list1.png"\] Alt text: Express List icon\).

3.  Edit the default columns in the pane.

    1.  Select the gear icon \(\[Omitted image "icon-gear-system-settings.png"\] Alt text: Gear icon\).

    2.  In the **Available columns** list, select the desired columns.

    3.  In the **Selected columns** list, drag selected columns up or down to reorder the fields. \[Omitted image "edit-list-columns.png"\] Alt text: Edit list columns dialog box

    4.  Select **Restore to column default** to return the columns to the default state.

    5.  Select **OK**.

4.  Modify the column width, order, and sort direction directly in the Express List pane.

    |Option|Action|
    |------|------|
    |**Column width**|Point to the right side of the column until the bi-directional arrow appears and drag the column to the desired width.|
    |**Column order**|Select the column header and drag it to the desired location.|
    |**Column sort**|Select the column header and then select the arrow. The arrow direction indicates the sort order. Each selection of the arrow changes the sort direction.|


## Result

The layout is automatically saved in the User preference \[sys\_user\_preference\] table. When you reopen the list, the same columns and order are displayed.

