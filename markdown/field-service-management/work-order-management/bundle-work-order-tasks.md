---
title: Bundle work order tasks
description: Manually bundle work order tasks from the platform so that agents can track and complete related tasks together instead of individually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/work-order-management/bundle-work-order-tasks.html
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-11-05"
reading_time_minutes: 1
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Bundle work order tasks

Manually bundle work order tasks from the platform so that agents can track and complete related tasks together instead of individually.

## Before you begin

Role required: wm\_admin

## About this task

When bundling tasks, note the following restrictions:

-   Tasks must be in the Pending Dispatch state to be added to a bundle.
-   Bundles can't be added to another bundle.
-   You can't add work order tasks that have dependencies or need a crew.
-   You can’t bundle tasks that have access hours, but you can add access hours to a bundle and its subtasks after you create it.
-   You can't create a sibling of a bundle that is in a bundle or create a sibling of a task that is in a bundle.
-   Tasks can't be schedule locked.
-   All subtasks must belong to the same assignment group. If territory management is enabled, they must also be in the same territory.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**.

2.  Select the check box for each task that you want to bundle.

3.  Select **Actions on selected rows...**.

4.  Select **Create bundle**.


## Result

The bundle is added to the My Bundles list.

