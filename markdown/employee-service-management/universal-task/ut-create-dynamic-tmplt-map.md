---
title: Create dynamic template mapping
description: Create dynamic templates to map fields on a Universal task form to corresponding fields on the parent table form. Dynamic templates help agents to map parent table fields to Universal task fields.
locale: en-US
release: yokohama
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Universal Task templates, Using Universal Task, Universal Task, Employee Service Management]
---

# Create dynamic template mapping

Create dynamic templates to map fields on a Universal task form to corresponding fields on the parent table form. Dynamic templates help agents to map parent table fields to Universal task fields.

## Before you begin

Ensure that you have write access to the parent table that is used for the template mappings.

Role required: sn\_uni\_task.template\_admin

## About this task

Dynamic template mappings can be created for templates that have an assigned parent table. In a dynamic mapping, the value of a field is updated with the value of the mapped field in the parent table. Dynamic template mappings get precedence over static template mappings. In static template mappings, fields are set to specific values. For more information on how to create a static template, see [Create a template using the Universal Task template form](ut-create-task-template.md).

## Procedure

1.  Navigate to **Universal Task** &gt; **Task Templates** &gt; **All**.

2.  Open the template that you want to create mappings for.

3.  In the Universal Task Dynamic Template Mappings related list, click **New**.

4.  In the **Universal task field** field, select the field that must be mapped.

5.  In the **Parent table field** field, select the field that must be mapped to the previously selected field from the **Universal task field** field.

    Depending on what type of field is selected in the **Universal task field** field, the **Advanced** option appears. If you select the **Advanced** option, the following options are available based on the input type of the Universal task field.

<table id="choicetable_vwq_2yk_t4b"><thead><tr><th align="left" id="d649531e126">

Input type for the Universal task field

</th><th align="left" id="d649531e129">

Advanced options

</th></tr></thead><tbody><tr><td id="d649531e135">

**String, such as Short description**

</td><td>

The **Value** field appears. You can map your Universal task to multiple fields from the parent table. You can also add a text template.

</td></tr><tr><td id="d649531e147">

**HTML, such as Rich description**

</td><td>

The **Value** field appears. You can map your Universal task to multiple fields from the parent table. You can also add a text template.

</td></tr><tr><td id="d649531e159">

**Date field, such as Due date**

</td><td>

-   The **Date offset type** field appears.
-   If you set the **Date offset type** field to **Before** or **After**, then the **Date offset by** field appears.


</td></tr></tbody>
</table>6.  Click **Submit**.


## Result

A mapping was created for a specific Universal task field. You can repeat this procedure to map more fields.

**Parent Topic:**[Universal Task templates](../concept/ut-task-template-landing.md)

