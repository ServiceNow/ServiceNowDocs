---
title: Add a task to a case on the Retail Portal
description: Create a task within an existing case to assign specific work to a team member on the Retail Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/t\_add-task-portal.html
release: australia
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [add task, create task, portal, assign task]
breadcrumb: [Quick case and task creation for in-store issues, Retail]
---

# Add a task to a case on the Retail Portal

Create a task within an existing case to assign specific work to a team member on the Retail Service Portal.

## Before you begin

Role required: `sn_rtl_instore_ops.associate`, `sn_rtl_instore_ops.manager`, or `sn_rtl_instore_ops.manager_contributor`

## About this task

On the portal, **Add task** is available only from the case's overflow menu. The new task is linked to the case automatically.

## Procedure

1.  From the Retail Portal, open the case for which you want to add a task.

2.  From the overflow menu, select **Add task**.

3.  Complete the task form with the following fields:

    |Field|Description|
    |-----|-----------|
    |**Short Description**|A brief summary of the work to be completed \(required\).|
    |**Assigned To**|Optional. The store associate or store manager who completes the task. The picker isn't restricted by role, so area and region managers can also be selected, but they can't assign tasks themselves.|
    |**Priority**|Required. The urgency of this task relative to other work.|
    |**Due Date**|When this task should be completed.|
    |**Description**|Optional. Additional details about the task.|
    |**Assignment group**|Optional. The group to assign the task to.|
    |**Attachment**|Optional. A photo or file that supports the task.|

4.  Select **Submit**.

    The task is created under the case and appears on the case's **Tasks** tab. An unassigned task is in the Pending Assignment state. A task that's assigned when you create it starts in the Accepted state. When a task is assigned, the assignee gets a push notification in the Retail Mobile app.

5.  Optional: To assign, edit, or close the task, open it from the case's **Tasks** tab.

    For details, see [Work on a quick in-store task on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/t_work-adhoc-task-portal.md).


**Parent Topic:**[Quick case and task creation for in-store issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/c_adhoc-case-task-creation.md)

