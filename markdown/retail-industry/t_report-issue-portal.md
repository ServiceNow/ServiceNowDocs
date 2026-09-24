---
title: Report an issue on the Retail Portal
description: Create a new case using the Record Producer to quickly report an in-store issue on the Retail Service Portal, then add tasks and assign work to team members.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t\_report-issue-portal.html
release: brazil
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 1
keywords: [report issue, create case, portal, store manager, record producer]
breadcrumb: [Quick case and task creation for in-store issues, Retail]
---

# Report an issue on the Retail Portal

Create a new case using the Record Producer to quickly report an in-store issue on the Retail Service Portal, then add tasks and assign work to team members.

## Before you begin

Role required: `sn_rtl_instore_ops.associate`, `sn_rtl_instore_ops.manager`, or `sn_rtl_instore_ops.plan_author`

## About this task

**Note:** The store field auto-populates based on your assigned store. Only Store Managers can reassign or close a case.

## Procedure

1.  From the Retail Portal, select the **Report an Issue** catalog item.

2.  Complete the following required fields:

    |Field|Description|
    |-----|-----------|
    |**Store**|The store associated with this issue. For Store Associates and Managers, this field auto-populates and is read-only. Area/Region Managers must select the store.|
    |**Short Description**|A brief, one-line summary of the issue \(for example, "Broken freezer in aisle 3"\).|
    |**Priority**|The urgency level of the issue \(required\).|
    |**Description**|Optional. A detailed explanation of the issue, including any context or location information.|
    |**Attachment**|Optional. Attach a photo or document to support the issue report.|

3.  Select **Submit**.

    **Note:** The system creates a case in New state and displays a confirmation with the case number. If you are the store manager, the case is auto-assigned to you. Otherwise, it is unassigned and awaiting triage.

4.  From the confirmation or case list, open the case and select **Add Task** to assign work to a team member.

    You can add multiple tasks to a single case. Each task represents a specific action item that one team member will complete. See [Add a task to a case on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/t_add-task-portal.md).


**Parent Topic:**[Quick case and task creation for in-store issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/c_adhoc-case-task-creation.md)

