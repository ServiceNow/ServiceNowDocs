---
title: Add state field policies to a change model state
description: Make change request fields mandatory or read-only in a specific state of a change model by adding state field policies to the model state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/define-state-field-policies.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [state field policies, change model, mandatory fields, read-only fields, change request]
breadcrumb: [State field policies for change models, Create a Change model, Configure, Change Management, IT Service Management]
---

# Add state field policies to a change model state

Make change request fields mandatory or read-only in a specific state of a change model by adding state field policies to the model state.

## Before you begin

The change model and its states must exist before you add policies. To set up model states, see [Configure change model states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-model-states.md).

Role required: none.

**Note:** Write access to the change model is required to add state field policies to the model state.

## About this task

Each policy controls one field in one state. To control multiple fields, add one policy per field.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Models**.

2.  Select the change model to update.

3.  In the **Model States** related list, select the state to add field policies to.

4.  In the **State Field Policies** related list, select **New**.

5.  Complete the State Field Policy form.

<table id="table-state-field-policy-form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Change request field that the policy applies to. The list shows fields from the table that the change model is based on.

</td></tr><tr><td>

**Mandatory**

</td><td>

Requires a value in the field while the change request is in this state. Selecting this check box also adds the field to a **State Field Policy Managed** transition condition on every transition into this state.

</td></tr><tr><td>

**Read Only**

</td><td>

Blocks changes to the field while the change request is in this state.

</td></tr><tr><td>

**Application**

</td><td>

Application scope that owns the policy. Controls which application the policy is associated with for update set tracking.

</td></tr><tr><td>

**Active**

</td><td>

Applies the policy to change requests in this state. Selected by default.**Note:** Set the Active check box to enable the policy. A field can be marked as mandatory, read-only, or both for the same state.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

The policy is active for change requests that use the model when they're in the selected state. If you selected **Mandatory**, change requests can't move into the state until the field has a value.

## What to do next

Open a record that uses this change model and set its state to the state that you configured. The field that you selected now appears as mandatory or read-only on the form.

If the field is mandatory, the system also creates or updates a **State Field Policy Managed** transition condition on every model state transition that leads into that state. For more information, see [State field policies for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-field-policies-change-models.md).

**Parent Topic:**[State field policies for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-field-policies-change-models.md)

**Related topics**  


[State field policies for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-field-policies-change-models.md)

[Default state field policies in base system change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/default-state-field-policies.md)

