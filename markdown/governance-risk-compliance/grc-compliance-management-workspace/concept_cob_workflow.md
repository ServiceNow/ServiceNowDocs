---
title: Control objective workflow
description: The control objective workflow introduces a review and approval process for changes to control objective records, preventing unreviewed updates from immediately affecting downstream objects such as controls.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Control objective workflow

The control objective workflow introduces a review and approval process for changes to control objective records, preventing unreviewed updates from immediately affecting downstream objects such as controls.

## Why the workflow exists

Before the control objective workflow, any user with the compliance user role could directly update a control objective record without a review process. Because control objectives are referenced by controls, policies, issues, and other objects, unreviewed changes would immediately affect all downstream records.

When you revise a published control objective, a working draft record is created to hold draft changes. The published record remains active and available to downstream processes until you explicitly publish the approved staging changes. The staging record is linked to the current version record and is always inactive, regardless of its workflow state.

For example, a control objective might require monthly sprinkler testing. If a compliance author wants to change the interval to two months, the existing published record continues to drive exception management and attestation while the proposed change goes through review and approval in the staging record. If the change is not approved, the published record is unaffected.

## Control objective workflow states

When the workflow property is enabled, a control objective moves through the following states:

-   **Draft**

    The initial state for a new or revised control objective. The record is inactive. Users listed in the **Owner** field, members of groups listed in the **Owning Group** field, and users with the compliance manager role can edit the record and perform workflow actions.

-   **Review**

    Triggered when the owner selects **Request Review**. Approvals are generated based on configured dynamic approval rules. If no approval rules apply, the control objective moves directly to Approved. The record is read-only during review.

-   **Approved**

    The control objective has passed all required approvals. The record is read-only except for the **Effective Date** field. The control objective is not yet active.

-   **Published**

    The control objective is active. The active flag is set to true. Core content fields \(name, description, supplemental guidance, category, classification, and type\) are locked. Metadata fields such as attestation settings and issue grouping rule, and ownership fields, remain editable without requiring a staging record.

-   **Retired**

    The control objective is inactive. The active flag is set to false. Retirement is triggered by selecting the **Retire** button or by setting the active flag to false directly.


## Revision types

When you initiate a change on a published control objective, you must select a revision type. The revision type determines how associated controls are affected when the change is published.

-   **Major**

    Use for substantive changes to the meaning or intent of the control objective. When a major revision is published, all associated controls move back to Draft, requiring control owners to review the changes and re-attest.

-   **Minor**

    Use for corrections such as spelling fixes, typo corrections, or rewording that does not change the functional meaning of the control objective. When a minor revision is published, associated controls remain in their current states. Updated field values are applied to controls without triggering re-attestation.


The categorization of a change as major or minor is subjective and is not enforced by field-level restrictions. Reviewers can reject a staging record if the revision type does not match the scope of the changes made. You can change the revision type at any point before publishing by selecting **Update Revision Type** on the staging record.

## Behavior with the workflow property enabled and disabled

The control objective workflow is controlled by the **Enable control objective workflow** property. The following table summarizes how behavior differs based on the property setting.

<table><thead><tr><th>

Behavior area

</th><th>

Property disabled

</th><th>

Property enabled

</th></tr></thead><tbody><tr><td>

Who can edit a control objective

</td><td>

Any user with the compliance user role

</td><td>

Users in the **Owner** field, members of groups in the **Owning Group** field, and users with the compliance manager role

</td></tr><tr><td>

Editing a published record

</td><td>

Direct edits to the control objective record

</td><td>

Edits are made on a staging record; the published record is not changed until staging changes are approved and published

</td></tr><tr><td>

State field

</td><td>

Present but no workflow transitions. New records default to Draft; active records show Published; inactive records show Retired

</td><td>

Full workflow transitions: Draft → Review → Approved → Published → Retired

</td></tr><tr><td>

Workflow actions

</td><td>

Not available

</td><td>

Available in workspace based on current state and user role \(Request Review, Publish, Retire, and others\)

</td></tr><tr><td>

Owner and Owning Group fields

</td><td>

Not present on the form

</td><td>

At least one of these fields is required

</td></tr><tr><td>

Effective Date field

</td><td>

Not available

</td><td>

Optional; automatically publishes the control objective on the specified date; populated with the actual publish date when left blank

</td></tr><tr><td>

Impact on controls when a change is published

</td><td>

All associated controls move to Draft immediately on save

</td><td>

Major revision: associated controls move to Draft. Minor revision: associated controls remain in their current states; updated field values are applied without triggering re-attestation

</td></tr><tr><td>

Control objective activation on policy publish

</td><td>

All associated control objectives are automatically activated when a policy is published

</td><td>

All associated control objectives must be in Approved or Published state before a policy can request approval. Approved control objectives are automatically published when the associated policy is publishedSimilarly, changes to a control objective cannot be published if an associated policy is in Published, Retired, or pending-approval state. To publish control objective changes, the associated policy must be in Draft or Review state.

</td></tr><tr><td>

Classic UI support

</td><td>

Full edit and related-list access

</td><td>

Edit and related-list access preserved; workflow actions available in workspace only. An info message on the form directs users to open the record in workspace to perform additional actions

</td></tr></tbody>
</table>