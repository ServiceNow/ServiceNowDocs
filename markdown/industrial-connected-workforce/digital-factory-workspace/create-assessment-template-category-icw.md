---
title: Create an assessment template category
description: Set up an assessment template category so that you can build standard templates for that category and use them in the Standards hub.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using templates to create standards, Industrial Guided Tasks, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create an assessment template category

Set up an assessment template category so that you can build standard templates for that category and use them in the Standards hub.

## Before you begin

Role required: sn\_icw.admin

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**.

2.  Select **New**.

3.  On the Assessment template category form, fill in the fields.

    For a description of the field values, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md). The Category role must be sn\_icw\_igt.user or any role that contains this role, such as sn\_icw\_igt.expert, sn\_icw\_igt.author, or any other role that you create.

<table id="table_axz_wxx_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique meaningful name for the template category.

</td></tr><tr><td>

Category role

</td><td>

Minimum role that you must have to view any template that is a member of this category. The role must be sn\_icw\_igt.user or any role that contains this role, such as sn\_icw\_igt.expert, sn\_icw\_igt.author, or any other role that you create.

</td></tr><tr><td>

Description

</td><td>

Text that helps others to understand the purpose of including templates in this category.

</td></tr><tr><td>

Active

</td><td>

Option to activate the category. By default, newly defined template categories are active.

</td></tr><tr><td>

Enable Normalization

</td><td>

Option to enable the use of normalization strategies for assessment templates in this category. Normalization allows advanced scoring calculations that adjust raw scores for guided tasks. **Note:** For the default Industrial Guided Task template category, an ICW administrator can select this option to allow normalization on IGT scoring.

</td></tr><tr><td>

Normalization strategies

</td><td>

Available normalization strategies for the category. This field is available only when Enable Normalization is selected.

</td></tr><tr><td>

Default normalization strategy

</td><td>

Default normalization strategy applied for assessment templates in this category. This field is available only when Enable Normalization is selected.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The assessment template category appears in the list of categories that can be specified when designing an assessment template in the Digital Factory Workspace.

**Parent Topic:**[Using templates to create standards](../concept/creating-standards-from-templates.md)

