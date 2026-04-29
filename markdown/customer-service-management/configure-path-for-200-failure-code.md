---
title: Configure paths for different failure code conditions
description: Configure a path for each failure code condition to provide appropriate guidance to agents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure paths for different failure code conditions

Configure a path for each failure code condition to provide appropriate guidance to agents.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

When the failure code received by the customer is 200, the path that leads to the Reassign case guidance is taken.

![Path for 200 error code conditions](../image/ex-200-failure-code-path.png)

For more information about how to configure a path, see [Determine the next node displayed in a decision tree](configure-path-in-gdb.md).

## Procedure

1.  In Decision Tree Builder, select the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on the Ask for failure codes question node.

    A new path and a new node are added to the canvas.

2.  Select the new path.

3.  In the **Path name** field, enter `200`.

4.  In the **Path priority** field, enter `100`.

5.  Select the appropriate fields to set the condition "Enter the failure code \| is \| true".

6.  Select **Save and close**.


## What to do next

Configure paths for other failure codes:

-   300 failure code - This path leads to the Create work order guidance.
-   500 failure code - This path leads to the Assign IT technician guidance.

