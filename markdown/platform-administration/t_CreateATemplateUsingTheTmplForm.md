---
title: Create a template using the Template form
description: Create a template record for any table to populate certain fields automatically.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Form templates, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a template using the Template form

Create a template record for any table to populate certain fields automatically.

## Before you begin

Role required: template\_editor\_global or admin

## About this task

Create a template using the Template form.

Templates allow users to more quickly and uniformly complete records.

The video above shows you how to complete the procedure below to create a template using the Template form.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Templates**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_tny_vtb_rq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this template.**Note:** The template name can't match an existing table name.

</td></tr><tr><td>

Table

</td><td>

Table that this template applies to. Select **Global** to make the template available for use with all tables.**Note:** The table list shows only the tables and database views that are in the same scope as the template.

</td></tr><tr><td>

Active

</td><td>

Option for making the template available for use. A template must be active to be used.

</td></tr><tr><td>

User

</td><td>

User who can configure and apply the template. If you define a user, no other users can see the template unless you select the **Global** option.

</td></tr><tr><td>

Groups

</td><td>

Group whose members can configure and apply the template. If you define a group, no other groups can see the template unless you select the **Global** option.

</td></tr><tr><td>

Global

</td><td>

Option to enable any user who can access the templates to view and apply this template.

</td></tr><tr><td>

Short description

</td><td>

Description of the template. **Note:** Adding content to this field doesn’t add that content to the **Short description** field of the forms that use this template.

</td></tr><tr><td>

Template

</td><td>

Content that automatically populates records that are based on this template. Select a field from the specified table in the left column and then enter the data to populate automatically in the right column.**Note:** Even though you can select dot-walked fields in the template, they don’t apply to fields that are on the form.

</td></tr><tr><td>

Link element

</td><td>

Template that links a child table with the template for the parent table. In the template for the child table, set the value to the field that references the parent table. After you set the value, the child template is explicitly linked to the parent table. **Note:** This field doesn’t appear by default. Configure the template form to add the field.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

See [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Parent Topic:**[Using form templates](../concept/c_Templates.md)

**Related topics**  


[Create templates for related task records](create-templates-for-related-task-records.md)

[Create a template by saving a form](t_SaveAFormAsATemplateInUI16OrUI15.md)

[Schedule record creation from a template](t_ScheduleATemplate.md)

[Create a module for a template](t_CreateAModuleForATemplate.md)

[Template bar](../concept/template-bar.md)

[Toggle the template bar](t_ToggleTheTemplateBar.md)

[Scripted templates](../reference/r_ScriptedTemplates.md)

