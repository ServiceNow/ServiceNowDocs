---
title: Change Management Workflow Studio actions
description: Use Workflow Studio actions as building blocks to handle the Change models and types. The flow actions are available under the ITSM spoke in Workflow Studio.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Workflow Editor, Workflow, Flow]
breadcrumb: [Change flows, Reference, Change Management, IT Service Management]
---

# Change Management Workflow Studio actions

Use Workflow Studio actions as building blocks to handle the Change models and types. The flow actions are available under the ITSM spoke in Workflow Studio.

<table id="table_wtp_v3v_bnb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply Change Approval Policy

</td><td>

Controls the approval process for a change request by creating user and group approvals according to a change approval policy record. Multiple actions can be used in a flow, where each action references the same or different Change approval policies.

</td></tr><tr><td>

Cancel Change Tasks from Flow

</td><td>

Cancels all related pending and open change tasks that are created from a flow.

</td></tr><tr><td>

Check Change for User Approval

</td><td>

Checks if the specified user has already approved the change request.

</td></tr><tr><td>

Disregard change approvals

</td><td>

Sets all related pending approvals to no longer required.

</td></tr><tr><td>

Evaluate Change Model

</td><td>

Evaluates the Change Model associated with this change request against the current state of the Change Request.

 Evaluating the change model evaluates all applicable conditions, determines if the state should be changed and changes it if one matches.

</td></tr></tbody>
</table>**Parent Topic:**[Change flows](change-flows.md)

