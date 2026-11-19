---
title: Create a work order task bundle
description: Bundle work order tasks from Dispatcher Workspace to group related visits, such as unplanned site visits and scheduled maintenance, and help reduce agent drive time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/create-work-order-task-bundle.html
release: brazil
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Bundling WOTs, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Create a work order task bundle

Bundle work order tasks from Dispatcher Workspace to group related visits, such as unplanned site visits and scheduled maintenance, and help reduce agent drive time.

## Before you begin

Role required: wm\_dispatcher

## About this task

When bundling tasks, note the following restrictions:

-   Tasks must be in the Pending Dispatch state to be added to a bundle.
-   Bundles can't be added to another bundle.
-   You can't add work order tasks that have dependencies or need a crew.
-   You can’t bundle tasks that have access hours, but you can add access hours to a bundle and its subtasks after you create it.
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

