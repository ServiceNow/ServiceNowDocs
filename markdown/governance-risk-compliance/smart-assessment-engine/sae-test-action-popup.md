---
title: Settings in the Test action pop-up window
description: You can select Test on the Trigger Smart Assessment action form to test the design of an Smart Assessment Engine assessment. You then specify the settings for the test in the Test action pop-up window.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Settings in the Test action pop-up window

You can select **Test** on the Trigger Smart Assessment action form to test the design of an Smart Assessment Engine assessment. You then specify the settings for the test in the Test action pop-up window.

## Test action pop-up window

<table id="table_krg_p53_2yb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment template

</td><td>

Assessment template that is the basis for the generated assessments.

</td></tr><tr><td>

Assessors

</td><td>

Persons who are notified of the assessment and typically respond to the assessment or assign it to another user. One assessment instance is assigned to each assessor.

 Assessors have the Assessment actor \[sn\_smart\_asmt.actor\] role. See [Roles in Smart Assessment Engine](sae-roles-defined.md).

</td></tr><tr><td>

Requester

</td><td>

Contact for questions from the assessor. Each generated assessment includes the contact information.

</td></tr><tr><td>

Description

</td><td>

Text that helps others to understand the intent of the generated assessments.

</td></tr><tr><td>

Template category

</td><td>

Category that the assessment template should be a member of. For example, Risk, Performance, Security, Personal data, and so on.

Template purposes enforce data segregation for templates. A purpose controls which users can view a template. Each assessment template is associated with a purpose. To view a template within a specific purpose, you must have a category role associated with that purpose.

For more information, see [Create an assessment template category](../task/sae-asmnt-template-category-create.md).**Note:** You can create an assessment only from a published assessment template. You can update a published template only if no active assessment is associated with the template.

</td></tr><tr><td>

Assessment target

</td><td>

Table records that are selected to be assessed, otherwise known as the assessment scope. Multiple tables can be added as the assessment target, which makes the scope a combination of records from each table.

</td></tr></tbody>
</table>