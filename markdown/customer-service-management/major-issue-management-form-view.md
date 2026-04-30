---
title: Major Case form view
description: Major issue management provides the Major Case form view, which includes the Major Case Information form section and the Child Cases related list.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Major issue management overview, Administer, Customer Service Management]
---

# Major Case form view

Major issue management provides the Major Case form view, which includes the Major Case Information form section and the Child Cases related list.

The Major Case form view does not display account-related information because a major case is not linked to a specific account, contact, or consumer. This information is stored in the child cases associated with a major case.

## Major Case Information form section

Major cases and major case candidates include the Major Case Information form section which includes the following fields.

<table id="MajorCaseFormSection"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Major case state

</td><td>

A major case can be in one of these states:-   **Proposed**: the initial state when a candidate case is created or proposed by an agent or manager.
-   **Accepted**: the Initial state when a major case is created by a manager or when a candidate case is promoted by a manager.
-   **Rejected**: the candidate case is rejected by a manager.
-   **Cancelled**: the case is cancelled.

</td></tr><tr><td>

Business impact

</td><td>

The business impact of the issue identified in the major case.

</td></tr><tr><td>

Probable cause

</td><td>

The probable cause of the issue identified in the major case.

</td></tr><tr><td>

Affected Customers

</td><td>

The recipients list selected for the major case. Child cases are created for the accounts or consumers included in the recipients list. This field is only visible when the major case state is Accepted.

</td></tr></tbody>
</table>Customer service agents can update the **Business impact** and **Probable cause** fields as well as add **work notes**. Major issue managers can update the **Business Impact** and **Probable Cause** fields and attach a recipients list. The **Affected Customers** field is only visible when the major case state is Accepted.

The **Work notes** field on the major case form is updated when a major case is proposed or a candidate case is created manually. The **Work notes** field on associated child cases is updated when a major case is accepted.

When a major issue manager rejects a candidate case, the **Major Case State** field is set to Rejected and the **Work notes** field is updated with the case state. The candidate case reverts to a regular case.

## Child Cases related list

Major issue management adds the **Child Cases** related list to the Customer Service Case form. All child cases associated with a major case are added to this list. Child cases are created automatically from the recipients list and can also be added or removed manually.

