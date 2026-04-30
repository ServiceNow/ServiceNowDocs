---
title: Create an assessment template category
description: Create an assessment template category in the Smart Assessment Engine application so that you can organize and grant access to the assessment templates that are related.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create an assessment template, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create an assessment template category

Create an assessment template category in the Smart Assessment Engine application so that you can organize and grant access to the assessment templates that are related.

## Before you begin

Role required: sn\_smart\_asmt.assessment\_admin

## About this task

Template purposes enforce data segregation for templates. A purpose controls which users can view a template. Each assessment template is associated with a purpose. To view a template within a specific purpose, you must have a category role associated with that purpose.

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

Description

</td><td>

Text that helps others to understand the purpose of including templates in this category.

</td></tr><tr><td>

Active

</td><td>

Option to activate the category.

 By default, newly defined template categories are active.

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


