---
title: Create a work order task bundle
description: Bundle tasks to enable agents to track multiple tasks in one work order task rather than individually. Minimize drive time by combining unplanned site visits with scheduled maintenance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Bundling work order tasks, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Create a work order task bundle

Bundle tasks to enable agents to track multiple tasks in one work order task rather than individually. Minimize drive time by combining unplanned site visits with scheduled maintenance.

## Before you begin

Role required: wm\_dispatcher

## About this task

When bundling tasks, note the following restrictions:

-   Tasks must be in the Pending Dispatch state to be added to a bundle.
-   Bundles can't be added to another bundle.
-   You can't add work order tasks that have dependencies, need a crew, or have a fixed access window to a bundle.
-   Vendor tasks can't be added to a bundle.
-   You can't create a sibling of a bundle that is in a bundle or create a sibling of a task that is in a bundle.
-   Tasks can't be schedule locked.
-   All subtasks must belong to the same assignment group. If territory management is enabled, they must also be in the same territory.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **My Dispatch Queue**.

2.  Select the tasks that you want to bundle.

3.  Select **Actions on selected rows...**.

4.  Select **Create bundle**.


## Result

The bundle is added to the My Bundles list.

