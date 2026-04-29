---
title: Configure activity stream tile colors
description: Administrators can control how activity tile colors display in the activity stream for both collapsed and expanded views.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure activity stream tile colors

Administrators can control how activity tile colors display in the activity stream for both collapsed and expanded views.

## Before you begin

-   Role required: admin
-   A tile color must be configured using the **Workspace activity stream background** attribute. The **Workspace activity stream apply variant** attribute only controls where that color is applied \(border only, or border and background\).

## About this task

You can control whether the activity stream tile color appears on the border only or on both the border and background. By default, collapsed tiles show color on the border only, while the expanded tiles show color on both border and background.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  In the **Table** field, filter for the task table.

3.  In the **Column name** field, open either *work\_notes* or *comments*.

    **Note:** These fields must be of type Journal Input for the attribute to work correctly.

4.  In the **Attributes** related list, click **New**.

5.  Enter the following attribute information:

    -   **Attribute name**: **Workspace activity stream apply variant**
    -   **Value**: Select one of the following options:

        |Option|Description|
        |------|-----------|
        |BORDER\_ONLY|Applies variant colors only to the border of the tile in both collapsed and expanded views.|
        |BORDER\_AND\_BACKGROUND|Applies variant colors to both the border and background of the tile in both collapsed and expanded views.|

6.  Click **Submit**.

7.  Refresh the activity stream to view the changes.


