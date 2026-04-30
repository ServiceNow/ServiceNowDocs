---
title: Create templates for related task records
description: Administrators can create a template for a Task table record that also creates one or more related records in the child Task table.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Form templates, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create templates for related task records

Administrators can create a template for a Task table record that also creates one or more related records in the child Task table.

## Before you begin

Role required: admin

## About this task

Administrators must understand the parent-child relationships between Task tables. For example, the Change Task table is a child of the Change table and the Incident Task table is a child of the Incident table.

**Note:** Child templates can only be applied automatically if you first apply the parent template from a module.

## Procedure

1.  From the parent Task table template, [configure the form layout](../concept/configure-form-layout.md#) to add these fields.

    -   **Next Related Child Template**
    -   **Next Related Template**
    -   **Link element**
2.  [Create a template](t_CreateATemplateUsingTheTmplForm.md) for the parent Task table.

    For example, create this template for the Change table.

<table id="table_jjb_hkw_1y"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Add server to network

</td></tr><tr><td>

Table

</td><td>

Change \[change\_request\]

</td></tr><tr><td>

Short description

</td><td>

Set up a server on the network

</td></tr><tr><td>

Template

</td><td>

-   \[Short description\]\[Set up server on the network\]
-   \[Category\]\[Hardware\]
-   \[Assignment group\]\[Hardware\]


</td></tr></tbody>
</table>3.  [Create a template](t_CreateATemplateUsingTheTmplForm.md) for the first related task.

    For example, create this template for the Change Task table.

<table id="table_tvy_llw_1y"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Order server

</td></tr><tr><td>

Table

</td><td>

Change Task \[change\_task\]

</td></tr><tr><td>

Short description

</td><td>

Order server hardware

</td></tr><tr><td>

Template

</td><td>

-   \[Short description\]\[Order server hardware\]
-   \[Assignment group\]\[Hardware\]


</td></tr><tr><td>

Link element

</td><td>

Change request

</td></tr></tbody>
</table>4.  [Create a template](t_CreateATemplateUsingTheTmplForm.md) for each additional related task.

    For example, create one additional template for the Change Task table.

<table id="table_tnt_rmw_1y"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Install server on network

</td></tr><tr><td>

Table

</td><td>

Change Task \[change\_task\]

</td></tr><tr><td>

Short description

</td><td>

Install server on network

</td></tr><tr><td>

Template

</td><td>

-   \[Short description\]\[Install server on network\]
-   \[Assignment group\]\[Hardware\]


</td></tr><tr><td>

Link element

</td><td>

Change request

</td></tr></tbody>
</table>5.  From the parent Task table template, set **Next Related Child Template** to the first related child task.

    For example, in the Add server to network template, select `Order server` in the **Next Related Child Template** field.

    ![Example for parent task template.](../image/ParentTaskTemplateExample.png)

6.  For each child related task, set **Next Related Template** to the next related task template.

    For example, in the Order server template, select `Install server on network` in the **Next Related Template** field.

    ![Example for child task template.](../image/ChildTaskTemplateExample.png)

    **Note:** The last related task template does not have a value for **Next Related Template**. For example, the **Install server on network** template does not have a value in **Next Related Template**.


## What to do next

[Create a module](t_CreateAModuleForATemplate.md) for the parent Task table template so that child templates can be applied to related task records. For example, create a module for **Add server to network**.

**Parent Topic:**[Form templates](../concept/c_Templates.md)

**Related topics**  


[Create a template using the Template form](t_CreateATemplateUsingTheTmplForm.md)

[Create a template by saving a form](t_SaveAFormAsATemplateInUI16OrUI15.md)

[Create records based on a template](t_ScheduleATemplate.md)

[Create a module for a template](t_CreateAModuleForATemplate.md)

[Template bar](../concept/template-bar.md)

[Toggle the template bar](t_ToggleTheTemplateBar.md)

[Scripted templates](../reference/r_ScriptedTemplates.md)

