---
title: Create predefined transition condition types
description: Create predefined transition conditions to reuse the conditions for your change models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/create-predefined-transition-condition-type.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Create predefined transition condition types

Create predefined transition conditions to reuse the conditions for your change models.

## Before you begin

Role required: change\_manager

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Module** &gt; **Change Model Condition Types**.

    A list of transition conditions for change requests appears.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_xm3_5nv_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the condition type. This name is displayed in the **Requires** field on the Model State Transition Condition form.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the condition type.

</td></tr><tr><td>

Table name

</td><td>

Table name that the condition is based on.

</td></tr><tr><td>

Condition \(Condition builder\)

</td><td>

Conditions that must be fulfilled for processing the transition.

</td></tr><tr><td>

Condition \(Script\)

</td><td>

Script that runs against the record in the **Table name** field and returns `true` when the transition can proceed. This field appears when **script** is selected in the **Condition Type** field.This field is available only when **Transition Script** is selected from **Requires** field.

**Note:** To edit this field, . Without it, the script editor is read-only. For more information, see [Model script editor role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/model-script-editor-roles.md).

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Open the **Change Model**, select the relevant **Model State** and either add or edit a Model State Transition that references the condition type.

    **Note:** Creating a condition type does not enable a transition on its own. To apply it, select the condition type in the **Requires** field of a model state transition condition.


**Parent Topic:**[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md)

**Related topics**  


[Attach a process for Change model states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/attach-process-change-model.md)

[Configure state model transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ConfigStateModelTransit.md)

