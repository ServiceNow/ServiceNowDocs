---
title: Review and approve time sheets
description: Managers can review time cards and time sheets for agents in their assignment groups.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Record the time worked on a work order task, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Review and approve time sheets

Managers can review time cards and time sheets for agents in their assignment groups.

## Before you begin

Role required: wm\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Time Sheets - Pending Approval**.

2.  Select a time sheet.

3.  If necessary, review the time cards associated with this time sheet in the **Time Cards** related list.

4.  Click one of the following.

    |Option|Description|
    |------|-----------|
    |**Approve**|The state of the time sheet and the associated time cards changes to **Approved** and becomes read-only. Time cards for any work order tasks that are in the **Work in process** state are marked as **Processed**. Once the work order task is **Complete**, the time cards are marked as **Approved**.|
    |**Reject**|The state of the time sheet and the associated time cards changes to **Rejected**. The field service agent can make changes to the time sheet and submit again for approval.|

    If rate cards are applicable for the time worked, expense lines are generated as part of the time sheets. Users with the financial\_mgmt\_user role can view these expense lines.


**Parent Topic:**[Record the time worked on a work order task](../concept/Recording-time-spent-on-work-order-tasks.md)

