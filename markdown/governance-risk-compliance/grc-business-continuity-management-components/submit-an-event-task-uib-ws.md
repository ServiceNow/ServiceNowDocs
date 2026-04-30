---
title: Request an approval and approve the event
description: Approve the exercise in BCM UIB Workspace.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Request an approval and approve the event

Approve the exercise in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending**.

2.  Select an event for which you are an approver.

3.  Verify that all activated plans are closed; close the open plans before submitting the event for an approval.

    **Note:** Submitting a functional exercise or actual event for approval when an activated plan is still in the **Open** state results in an error message: `All activated plans must be closed before submitting the event for an approval`.

    ![Error message.](../image/event-error-msg.png)

4.  Select **Submit for approval**.

    **Note:** If an approval record is created for the exercise, the **Approve** or **Reject** actions are not displayed on the form. For a user to view the **Approve** or **Reject** actions, these conditions must be fulfilled:

    -   The user should have the sn\_recovery.event\_manager role.
    -   The exercise should be in the **Pending approval** state.
    -   The exercise should not have any approval records created.
5.  Select **Closed Complete**.

    You can update the state of the event to **Closed Complete**.


**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

