---
title: Create and publish a control objective
description: Create a control objective and move it through the workflow states from Draft to Published.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Control objective workflow, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create and publish a control objective

Create a control objective and move it through the workflow states from Draft to Published.

## Before you begin

Role required: sn\_compliance.user

The control objective workflow property must be enabled.

## About this task

When the control objective workflow is enabled, a new control objective must go through a review and approval process before it becomes active. The workflow moves the record through Draft, Review, and Approved states. Only after the record is published does it become active and available to downstream objects such as controls or policy exceptions.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Content Library** &gt; **Control Objectives**.

2.  Select **New**.

3.  Fill in the required fields, including the control objective name, description, and at least one of the following ownership fields:

    -   **Owner**: Add one or more users with the compliance user role or the library user role. If **Owning Group** is also populated, owners must be members of the owning group.
    -   **Owning Group**: Add one or more user groups. All members of the listed groups can edit the record and perform workflow actions.
4.  Select **Save**.

    The record is saved in Draft state and is inactive.

5.  Complete the content of the control objective, then select **Request Review** to submit the record for approval.

    The record moves to Review state. Approvals are generated based on configured dynamic approval rules. If no approval rules apply to the record, the record moves directly to Approved.

    **Note:** Approval rules must be configured before using the workflow. See [Configure approval rules for control objective review](task_configure_approval_rules.md) for configuration instructions.

6.  After all approvers approve the record, confirm that the state has changed to Approved.

    If an approver rejects the record, the state returns to Draft. Update the record to address the rejection reason, then select **Request Review** again.

7.  In the **Effective Date** field, enter the date on which the control objective should become active.

    If you set an effective date, a scheduled flow automatically publishes the control objective when that date is reached. You can still publish the record manually before the effective date if needed. If you do not set an effective date, the field is automatically populated with the date on which you manually publish the record.

    **Note:** Only users listed in the **Owner** field or members of groups in the **Owning Group** field can edit the **Effective Date** field when the record is in Approved state. All other fields on the form are read-only.

8.  Select **Publish** to make the control objective active.

    The record moves to Published state, the active flag is set to true, and the control objective becomes available to downstream objects. Core content fields \(name, description, supplemental guidance, category, classification, and type\) are locked on the published record.


