---
title: Trigger Smart Assessment action form
description: Use the Trigger smart assessment action form to add assessment actions to a flow or to obtain a code snippet for a script as part of the process for triggering Smart Assessment Engine assessments.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Trigger Smart Assessment action form

Use the Trigger smart assessment action form to add assessment actions to a flow or to obtain a code snippet for a script as part of the process for triggering Smart Assessment Engine assessments.

## Trigger Smart assessment action form

<table id="table_c25_3pw_vbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment template

</td><td>

Smart assessment template record to use to generate the assessment.

</td></tr><tr><td>

Assessors

</td><td>

Persons who are notified of the assessment and typically respond to the assessment or assign it to another user. One assessment instance is assigned to each assessor.

 Assessors have the Assessment actor \[sn\_smart\_asmt.actor\] role. See [Roles in Smart Assessment Engine](sae-roles-defined.md).

</td></tr><tr><td>

Collaborative assessment

</td><td>

Assessment which can have multiple contributors.**Note:** The 'Collaboration features for Smart Assessment' plugin must be installed for this to work.

</td></tr><tr><td>

Primary assessor \(Required for collaborative\)

</td><td>

Assessment owner for the collaborative assessment.

</td></tr><tr><td>

Requester

</td><td>

User that is the contact for questions from the assessor. Each generated assessment includes the contact information.

</td></tr><tr><td>

Due date

</td><td>

Due date that appears in the assessment.

 This setting overrides the **Duration** setting and the **Duration** setting in the template.

</td></tr><tr><td>

Duration

</td><td>

Time period that is used to calculate the due date of the assessment, starting from when the assessment is triggered.

 This setting overrides the **Duration** setting in the template.

</td></tr><tr><td>

Duplicate handling

</td><td>

Action to take when a duplicate assessment exists.

**Note:** An assessment is considered as a duplicate if there’s another open assessment with the same template, scope items, group, or assessors.

 -   **Do not create duplicate assessments**
-   **Create duplicate assessments**
-   **Create new and cancel existing assessments** Create an assessment to change the state of the existing assessment to **Cancelled**.

</td></tr><tr><td>

Assessment group

</td><td>

Assessment group that the generated assessments are associated with.

**Note:** The assessment group that you select should be in an open state and contain the assessments that are linked to the same assessment template as the one you are using.

 If you select an assessment group, the system checks whether the group is open or closed:

-   Open: The system first validates that the existing group contains at least one assessment that is linked to the same assessment template. If so, then generated assessments are added to the existing group.
-   Closed: Assessments can’t be added to the existing group.

 **Note:** If you don't select an assessment group, all generated assessments are grouped under a newly created group.

</td></tr><tr><td>

Scope

</td><td>

List of all scope items that the generated assessments are applied to.

 Each scope item contains two keys: `table` and `record`.

 For each context item that is configured at the template level, a corresponding scope item must be set up. For example, if the context items for a template include tables such as Controls \[sn\_compliance\_control\] and Entity \[sn\_grc\_profile\], then at least two scope items should be configured in the scope: one with `table: Entity [sn_grc_profile], record: [profile_record_id]` and another with `table: Controls [sn_compliance_control], record: [control_record_id]`.

 The table records to be assessed are also known as the assessment scope. You can add multiple scope items but not from the same table.

</td></tr></tbody>
</table>