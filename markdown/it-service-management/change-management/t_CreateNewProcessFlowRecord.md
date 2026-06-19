---
title: Create a process flow record
description: Create and add a process flow record for the Complete state. The process flow formatter displays at the top of the Change Request form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_CreateNewProcessFlowRecord.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "NewStateTutProcFlow1.png"\] Alt text: Process flow

5.  Click **Update**.


**Parent Topic:**[Tutorial: add a new change management state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_AddNewStateTutorial.md)

**Previous topic:**[Create a UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateNewUIAction.md)

**Next topic:**[Update the change request workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_UpdateWorkflow.md)

