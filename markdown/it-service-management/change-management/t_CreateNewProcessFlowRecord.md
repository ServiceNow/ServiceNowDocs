---
title: Create a process flow record
description: Create and add a process flow record for the Complete state. The process flow formatter displays at the top of the Change Request form.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference, Change Management, IT Service Management]
---

# Create a process flow record

Create and add a process flow record for the **Complete** state. The process flow formatter displays at the top of the Change Request form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Process Flow**.

2.  Open the **Normal Change – Implement state** record.

3.  Open the form context menu and click **Insert and Stay** to create a duplicate record.

4.  Modify the following fields with new values.

    |Field|Values|
    |-----|------|
    |Name|Normal Change – Complete State|
    |Label|Complete|
    |Order|550|
    |Condition|\[State\] \[is\] \[Complete\]|

    ![Process flow](../image/NewStateTutProcFlow1.png)

5.  Click **Update**.


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Create a UI action](t_CreateNewUIAction.md)

**Next topic:**[Update the change request workflow](t_UpdateWorkflow.md)

