---
title: Configure the maximum number of related records to display
description: Configure the maximum number of related records to display in the Related Records tab in the contextual side panel in CSM Configurable Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure dynamic related records, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure the maximum number of related records to display

Configure the maximum number of related records to display in the Related Records tab in the contextual side panel in CSM Configurable Workspace.

## Before you begin

Role required: ui\_builder\_admin, admin

## About this task

As part of configuring the Related Records shared page, the administrator can define the maximum number of related records that are displayed in the Related Records tab in the contextual side panel. This is defined as part of the UI Builder data transform configuration. The default value is 100 records.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the My experiences list, click the desired workspace.

3.  In the Page menu, select **Record**.

    The Page menu is in the upper left corner of the UI Builder interface.

4.  Click **Edit in original scope**.

5.  In the Content list below the Page menu, click the **Contextual sidebar** component.

6.  In the contextual sidebar configuration panel on the right side of the UI Builder interface, click the Config tab.

7.  In the Tabs list, click **Related Record**.

8.  Click **Edit Content**.

9.  Click the Data icon in the bar on the left side of the UI Builder interface.

10. Under Local data resource instances, click **Look Up Related Records**.

11. In the Configuration tab for the data resource, enter a value in the **Max results** field.

12. Click **Save**.


