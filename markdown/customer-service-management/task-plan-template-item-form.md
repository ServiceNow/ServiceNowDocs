---
title: Template item form
description: The Template item form displays details about a template item for a task plan template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/task-plan-template-item-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Template item form

The Template item form displays details about a template item for a task plan template.

The Template item form includes the following fields on the Details tab.

<table id="table_vyg_gzg_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated record number.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the template item.

</td></tr><tr><td>

Table

</td><td>

Select a table in which the system creates the template item record when the task plan template is applied.For example, if the template item is a case task, the system should create that item in the Case Task table \[sn\_customerservice\_task\].

</td></tr><tr><td>

Task plan template

</td><td>

Displays the number of the parent task plan template for this template item.

</td></tr><tr><td>

Order

</td><td>

The order in which the template item appears in the hierarchical list.

</td></tr><tr><td>

Parent

</td><td>

If the template item is a child of another template item, this field displays the parent item number.

</td></tr><tr><td>

Parent field identifier

</td><td>

The column on the selected table that captures the relationship to the parent template item.

</td></tr><tr><td>

Template item field identifier

</td><td>

The column on the selected table that captures the reference back to the template item that created the record. This field is available by default. The Case \[sn\_customerservice\_case\] and Case Task \[sn\_customerservice\_task\] tables include this column.This field is hidden on this form when the **Template item configuration** field on this record is populated, since the value is then taken from the referenced configuration record instead. To change the value, update the configuration and use **Save and cascade** to apply the change to existing template items.

</td></tr><tr><td>

Template execution field identifier

</td><td>

The column on the selected table that captures the reference to the template execution the record was created under. This field is available by default. The Case \[sn\_customerservice\_case\] and Case Task \[sn\_customerservice\_task\] tables include this column.This field is hidden on this form when the **Template item configuration** field on this record is populated, since the value is then taken from the referenced configuration record instead. To change the value, update the configuration and use **Save and cascade** to apply the change to existing template items.

</td></tr><tr><td>

Business organization field identifier

</td><td>

The column on the selected table that captures the reference to the associated service organization. This field is available only when the Multi Case plugin is active `com.sn_multi_case_creation`.This field is hidden on this form when the **Template item configuration** field on this record is populated, since the value is then taken from the referenced configuration record instead. To change the value, update the configuration and use **Save and cascade** to apply the change to existing template items.

</td></tr><tr><td>

Fields

</td><td>

This field appears when you select a table in the **Table** field. Specify the fields and the field values that the system should use to create the template item record. Use the **+**\|**x** buttons to add and delete rows.

</td></tr></tbody>
</table>