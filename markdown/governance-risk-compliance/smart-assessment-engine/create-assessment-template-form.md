---
title: Create assessment template form
description: Learn about the fields of the Create Assessment Template form. Use this form to create an assessment template.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an assessment template, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create assessment template form

Learn about the fields of the **Create Assessment Template** form. Use this form to create an assessment template.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template name

</td><td>

Unique meaningful name for the template.

</td></tr><tr><td>

Assessment name

</td><td>

Add separate assessment name ![](../image/separate-assessment-name.png)icon that includes an optional alternative name for generated assessments. The respondent sees this name rather than the template name.

</td></tr><tr><td>

Description

</td><td>

Text that helps others to understand what the template is being used for.

</td></tr><tr><td>

Purpose

</td><td>

Purpose that the new assessment template should be a member of. For example, Risk, Performance, Security, and so on.

Template purposes enforce data segregation for templates. A purpose controls which users can view a template. Each assessment template is associated with a purpose. To view a template within a specific purpose, you must have a category role associated with that purpose.

For more information, see [Create an assessment template category](../task/sae-asmnt-template-category-create.md)

</td></tr><tr><td>

Assessment target

</td><td>

Table records that are selected to be assessed, otherwise known as the assessment scope. Multiple tables can be added as the assessment target, which makes the scope a combination of records from each table.**Note:** Assessment targets \(context items\) are configured after the template is created, not during initial creation. Adding assessment targets requires the sn\_smart\_asmt.assessment\_admin role and can only be done while the template is in draft state.

</td></tr></tbody>
</table>