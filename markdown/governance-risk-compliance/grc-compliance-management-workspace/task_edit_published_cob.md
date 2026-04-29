---
title: Edit a published control objective
description: Revise a published control objective by creating a staging record, drafting changes, and publishing them after approval.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Control objective workflow, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Edit a published control objective

Revise a published control objective by creating a staging record, drafting changes, and publishing them after approval.

## Before you begin

Role required: sn\_compliance.user

## About this task

To revise a published control objective, you must create a staging record. The staging record holds all draft changes until they are approved and published. The published record remains active throughout the process, so downstream objects such as controls and policy exceptions continue to reference the current version.

Each control objective has at most one staging record. The staging record is reused for each subsequent edit cycle and is retained after publishing for audit purposes.

**Important:** You cannot publish changes to a control objective if it is associated with a published, retired, or pending-approval policy. To publish the changes, the associated policy must first be moved to Draft or Review state.

## Procedure

1.  Open the published control objective that you want to revise.

2.  Select **Edit**.

    A dialog box opens prompting you to select a revision type.

3.  Select the revision type and enter a justification, then select **Submit**.

    -   **Major**

        Select if the changes affect the meaning or intent of the control objective. When the change is published, all associated controls move back to Draft.

    -   **Minor**

        Select if the changes are corrections such as spelling fixes or rewording that does not affect the functional meaning. When the change is published, associated controls remain in their current states.

    A staging record is created and you are redirected to the working draft. The staging record is pre-populated with the field values from the current published version.

4.  Make the required changes to the fields on the staging record.

5.  Select **Save**.

6.  Select **Request Review** to submit the staging record for approval.

    Approvals are generated based on configured dynamic approval rules. If no approval rules apply, the record moves directly to Approved. To navigate between the staging record and the published record, use the **View Working Draft** and **View Published Version** buttons.

7.  After all approvers approve the staging record, confirm that its state has changed to Approved.

    If an approver rejects the record, the state returns to Draft. Update the staging record to address the rejection reason, then select **Request Review** again.

8.  In the **Effective Date** field, enter the date on which the changes should take effect.

    If you set an effective date, a scheduled flow automatically publishes the changes when that date is reached. You can still publish manually before the effective date if needed.

    **Note:** The **Effective Date** field is read-only if the control objective is associated with a published policy. To set an effective date in this scenario, the associated policy must first be moved to Draft or Review state.

9.  Select **Publish** to apply the changes to the published record.

    The field values from the staging record are copied to the current version record. If the revision type is Major, all associated controls move to Draft. If the revision type is Minor, associated controls remain in their current states and receive the updated field values without re-attestation being triggered.


