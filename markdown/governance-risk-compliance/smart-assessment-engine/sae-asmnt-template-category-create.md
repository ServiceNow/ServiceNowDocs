---
title: Create an assessment template category
description: Create an assessment template category in the Smart Assessment Engine application so that you can organize and grant access to the assessment templates that are related.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an assessment template, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create an assessment template category

Create an assessment template category in the Smart Assessment Engine application so that you can organize and grant access to the assessment templates that are related.

## Before you begin

Role required: sn\_smart\_asmt.assessment\_admin

## About this task

Template purposes enforce data segregation for templates. A purpose controls which users can view a template. Each assessment template is associated with a purpose. To view a template within a specific purpose, you must have a category role associated with that purpose.

Use the **Allow user delegation** field to let users delegate their assessments in this category.

If you use question banks, this form also includes a **Question bank category roles** field. This field controls access to the question banks associated with this category, separately from the **Category roles** field that controls access to templates. For more information, see [Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/question-bank.md).

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**.

2.  On the Assessment template categories list, select **New** and then fill in the form.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique meaningful name for the template category. For example, `Food storage compliance`.

</td></tr><tr><td>

Category roles

</td><td>

Specifies the minimum roles required to view templates within this category. To view a template, a user must have one or more of the roles associated with the category. This is a multi‑select field, allowing each category to be linked to multiple roles. Users assigned any of these roles inherit the corresponding permissions for all templates in the category.

</td></tr><tr><td>

Question bank category roles

</td><td>

Specifies the minimum roles required to access question banks associated with this category. To create or view a question bank, users must have one or more of these roles. They must also have a base question bank role, such as **question\_bank\_manager** or **question\_bank\_reader**. This is a multi-select field, allowing each category to be linked to multiple roles. This field is separate from Category roles, which governs access to templates.

</td></tr><tr><td>

Description

</td><td>

Text that helps others to understand the purpose of including templates in this category.

</td></tr><tr><td>

Active

</td><td>

Option to activate the category.

 By default, newly defined template categories are active.

</td></tr><tr><td>

Allow user delegation

</td><td>

Option that lets users with assignments in this category have another user act on their behalf, using the platform delegation feature. This option is off by default.

 When selected, a user can name a delegate who can act on their Smart Assessments in this category during a set period. For more information, see [Delegation in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/delegation-in-sae.md).

</td></tr><tr><td class="sub-head" colspan="2">

General settings

</td></tr><tr><td>

Enable quick edit

</td><td>

Automatically enables quick edit features when this category is assigned to an assessment template.

</td></tr><tr><td class="sub-head" colspan="2">

Set defaults for templates

</td></tr><tr><td>

Enable normalization

</td><td>

Automatically enables normalization when this category is assigned to an assessment template.

</td></tr><tr><td>

Normalization strategies

</td><td>

Normalization strategies available. This field appears only when **Enable normalization** field is selected.

</td></tr><tr><td>

Default normalization strategy

</td><td>

Default normalization strategy for an assessment assigned with this category. This field appears only when **Enable normalization** field is selected.

</td></tr></tbody>
</table>3.  Select **Submit**.

    The system generates the assessment template category and adds it to the list of categories that can be specified when designing an assessment template. Active categories are only available for use while categorizing templates.


