---
title: Add a task to a case on the Retail Portal
description: Create a task within an existing case to assign specific work to a team member on the Retail Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t\_add-task-portal.html
release: brazil
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 1
keywords: [add task, create task, portal, assign task]
breadcrumb: [Quick case and task creation for in-store issues, Retail]
---

# Add a task to a case on the Retail Portal

Create a task within an existing case to assign specific work to a team member on the Retail Service Portal.

## Before you begin

Role required: `sn_rtl_instore_ops.manager` or `sn_rtl_instore_ops.associate`

## About this task

**Note:** Tasks can be added from the **Tasks** tab on the case detail page or from the case **Overflow** menu. Task form fields match the case form for consistency.

## Procedure

1.  From the Retail Portal, open the case for which you want to add a task.

2.  Select the **Tasks** tab.

3.  Select **Add Task** \(or from the **Overflow** menu, select **Add Task**\).

4.  Complete the task form with the following fields:

    |Field|Description|
    |-----|-----------|
    |**Short Description**|A brief summary of the work to be completed \(required\).|
    |**Assigned To**|The person responsible for completing this task. Only team members assigned to the store are available \(required\). Area/Region Managers cannot be assigned to tasks.|
    |**Priority**|The urgency of this task relative to other work.|
    |**Due Date**|When this task should be completed.|
    |**Description**|Optional. Additional details about the task.|

5.  Select **Submit**.

    **Note:** The task is created in Pending Dispatch state and assigned to the selected team member. The assignee receives a notification on their mobile device if they have one registered.

6.  To edit or close the task, open it and use the **Overflow** menu. See [Work on a Store Task on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-in-store-task-portal.md) for task management steps.


**Parent Topic:**[Quick case and task creation for in-store issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/c_adhoc-case-task-creation.md)

