---
title: Create a problem task
description: Problem tasks are how the problem coordinator asks subject matter experts for help with identifying the root cause and proposed fix for a problem. Divide the problem into multiple problem tasks to help with the investigation. You can assign the problem tasks to different assignment groups or users.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Problems, Problem Management, IT Service Management]
---

# Create a problem task

Problem tasks are how the problem coordinator asks subject matter experts for help with identifying the root cause and proposed fix for a problem. Divide the problem into multiple problem tasks to help with the investigation. You can assign the problem tasks to different assignment groups or users.

## Before you begin

Role required: itil, sn\_problem\_write, admin, problem\_admin, problem\_coordinator, problem\_manager, or problem\_task\_analyst

## Procedure

1.  Navigate to **All** &gt; **Problem** &gt; **Open**.

2.  Open the problem record for which you want to create a problem task.

3.  In the related list of the problem record, click **Problem Tasks** and click **New**.

4.  Select any one of the following problem tasks.

    |Option|Description|
    |------|-----------|
    |**Root Cause Analysis**|Tasks where the problem coordinator requires help from subject matter experts to investigate the root cause of a problem and find a proposed fix for the problem|
    |**General**|All other tasks|

5.  On the form, fill in the fields.

    For a description of the field values, see [Problem Task form](../reference/problem-task-form.md).

6.  Click **Submit**.

    The problem task enters the **New** state. If you have filled the mandatory fields that are necessary to move a problem task record to the **Assess** state, the problem task record directly moves to the **Assess** state. If you want to add any additional field for the assess state, you must add the field at **System UI** &gt; **Form Sections**. For more information, refer [Add a field in the assess mandatory field dialog](add-field-in-assess-dialog-form.md).


## What to do next

Assess the problem task.

**Parent Topic:**[Managing Problems](../concept/problem-mgmt-lifecycle.md)

