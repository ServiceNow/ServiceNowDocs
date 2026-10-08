---
title: State field policies for change models
description: Use state field policies to make change request fields mandatory or read-only at each state in a change model. Policies are enforced on the form when a change request is created or updated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/state-field-policies-change-models.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 4
keywords: [state field policies, change model, mandatory fields, read-only fields, change request]
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# State field policies for change models

Use state field policies to make change request fields mandatory or read-only at each state in a change model. Policies are enforced on the form when a change request is created or updated.

A change model defines the states that a change request moves through, such as **New**, **Assess**, and **Authorize**. State field policies extend a change model by letting you mark specific fields as mandatory or read-only for each of those states.

A state field policy controls one field in one state of a change model. Each policy can make the field mandatory, read-only, or both when a change request that uses the model is in that state. Define state field policies on the model state record, in the **State Field Policies** related list.

Base system change models use state field policies to control mandatory fields. For example, the **Assignment group** field is made mandatory through a state field policy. For the policies included in the base system, see [Default state field policies in base system change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/default-state-field-policies.md).

## State field policy overview

Each state on a change model can have one or more state field policies. A state field policy identifies a field on the target table and sets whether that field is **Mandatory**, or **Read Only** while a record is in that state. These policies work the same way as UI policies on the platform, except that they are attached directly to the change model rather than to the table.

Attaching the policy to the change model means the same mandatory and read-only rules apply consistently to every change request that uses that model. No separate UI policy or client script on the change request table is required.

## How state field policies are enforced

Policies are applied on the change request form and enforced on the server when a change request is created or updated. This includes updates made through scripts, integrations, or APIs.

-   **Mandatory**: A change request can't be saved while a mandatory field is empty. The update is rejected with a message listing the missing fields, for example, `Mandatory fields must be populated: Close code`.
-   **Read Only**: A read-only field can't be changed. The update is rejected with a message listing the affected fields, for example, `Read-only fields can't be modified: Type`.

The following exceptions apply to read-only enforcement:

-   When a change request moves to a new state, only fields that are read-only in both the previous state and the new state are blocked. A field that is read-only only in the new state can still be updated in the same save that triggers the state change.
-   When a change request is created, field values set by the record preset of the change model aren't blocked.
-   If a field is both mandatory and read-only and has no value, you can enter a value for it one time.

## How state field policies combine with other rules

The mandatory and read-only fields for a change request are determined by combining rules from several sources:

-   State field policies for the current state and the state the change request is moving to.
-   Transition conditions of the **Mandatory Fields** type on the transition between the two states.
-   Template field policies from the change template used to create the change request.

## Automatically managed transition conditions

When you make a field mandatory in a state field policy, the system automatically adds a transition condition named **State Field Policy Managed**, of the **Mandatory Fields** type, to every transition into that state. This condition blocks a change request from moving into the state until the field has a value.

The system keeps these conditions in sync with the policy:

-   If you change the field in the policy, the condition is updated.
-   If you clear **Mandatory** or delete the policy, the field is removed from the condition. The condition is deleted when it has no fields left.
-   If you change the destination state of a transition, the managed condition is rebuilt for the new state.

If more than one state can transition into the same target state, the system keeps the mandatory field requirement in sync across all applicable transition conditions. For example, if a field is mandatory in the **Authorize** state, both a transition from **New** to **Authorize** and a transition from **Assess** to **Authorize** require that field. You do not need to update each transition condition yourself.

**Warning:** Don't edit **State Field Policy Managed** transition conditions directly. Manage mandatory fields through the state field policies instead.

## Copying change models

When you copy a change model, the state field policies defined on each model state are copied to the new model.

-   **[Add state field policies to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/define-state-field-policies.md)**  
Make change request fields mandatory or read-only in a specific state of a change model by adding state field policies to the model state.
-   **[Default state field policies in base system change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/default-state-field-policies.md)**  
The Change Management - Change Model Foundation Data plugin \(com.snc.change\_management.change\_model.foundation\) includes state field policies for the base system change models. All default policies make fields mandatory only.

**Parent Topic:**[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-a-change-model.md)

**Related topics**  


[Add state field policies to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/define-state-field-policies.md)

[Default state field policies in base system change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/default-state-field-policies.md)

[Configure change model states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-model-states.md)

