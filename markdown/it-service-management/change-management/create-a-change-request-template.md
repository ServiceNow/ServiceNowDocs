---
title: Create a change request template
description: You can create a template that can be used to create change requests with pre-defined supporting tasks. Templates simplify the process of submitting new records by populating fields automatically.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Create a change request template

You can create a template that can be used to create change requests with pre-defined supporting tasks. Templates simplify the process of submitting new records by populating fields automatically.

## Before you begin

Role required: admin

The administrator must configure the form layout to add these fields: **Next Related Template**, **Next Related Child Template**, **Link element**

## About this task

There are two change request template configuration items.

-   **Change\_request**: This object does not have a link element, because it is at root level.
-   **Change\_task**: This task object is one level below root level, so it uses the parent table as a link element.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Templates**.

2.  Click **New**.

3.  Complete the form as described in [Create a template using the Template form](https://www.servicenow.com/docs/access?context=t_CreateATemplateUsingTheTmplForm&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

4.  Complete the remaining fields, as appropriate.

<table id="table_m3q_gnv_lz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Next Related Template

</td><td>

A template at the same hierarchical level as the current template \(sibling\).Use this field on a child template to specify an extra child template under the same parent template. For example, you can use child templates to create multiple change tasks for a change request template and specify sibling child templates.

 This field is not supported on top-level templates.

</td></tr><tr><td>

Next Related Child Template

</td><td>

A template at the hierarchical level below the current template \(child\).You can assign a child template to a child template.

</td></tr><tr><td>

Link element

</td><td>

Specifies a link to a record created from a child template to the record created from the parent template.The template script chooses the first valid reference field that can link to the parent record when this field is left blank.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

