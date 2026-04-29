---
title: Create a module for a template
description: You can create a module to open a form with pre-populated template data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Form templates, Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a module for a template

You can create a module to open a form with pre-populated template data.

## Before you begin

Role required: admin

## About this task

Child templates are only applied if the parent template is applied from a module. Child templates are not applied by applying a template to a new form.

## Procedure

1.  Point to the application menu, such as **Self-Service**, and select the edit application \(pencil\) icon.

2.  In the **Modules** related list, select **New**.

3.  Fill in the **Title** and **Order** fields as appropriate.

4.  In the **Link Type** field, select **URL \(from Arguments\)**.

5.  In the **Arguments** field, enter `<table_name>.do?sys_id=-1&sysparm_template=<template_name>`

    The `<table_name>` is the name of the table you selected for the table field, for example `incident`. The `<template_name>` is the name of the template you want to use to pre-populate the form, for example `Incident_call_type`.

6.  Select **Submit**.

7.  Refresh the application navigator to view the new module.


**Parent Topic:**[Using form templates](../concept/c_Templates.md)

**Related topics**  


[Create a template using the Template form](t_CreateATemplateUsingTheTmplForm.md)

[Create templates for related task records](create-templates-for-related-task-records.md)

[Create a template by saving a form](t_SaveAFormAsATemplateInUI16OrUI15.md)

[Schedule record creation from a template](t_ScheduleATemplate.md)

[Template bar](../concept/template-bar.md)

[Toggle the template bar](t_ToggleTheTemplateBar.md)

[Scripted templates](../reference/r_ScriptedTemplates.md)

