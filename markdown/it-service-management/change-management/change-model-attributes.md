---
title: Change model attributes
description: Change model attributes are tags that you assign to states in a change model. Scripts can check which attributes are present in the current state of a change and turn functionality on or off for that state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/change-management/change-model-attributes.html
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [change model attributes, change model, model states, Change Management]
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Change model attributes

Change model attributes are tags that you assign to states in a change model. Scripts can check which attributes are present in the current state of a change and turn functionality on or off for that state.

A change model defines the states that a change request moves through. With change model attributes, you can also control what's allowed in each of those states. You define an attribute once, and then assign it to one or more states in a change model. Within a state, the attribute is available to both server-side and client-side scripting, so business rules, UI actions, and client scripts can check for it and trigger different behaviors.

## How change model attributes work

Each attribute has a label, a name, an optional description, and a table. You can define attributes only for the Change Request \[change\_request\] table or tables that extend it. An attribute defined on a table is available for all extensions of that table.

A new attribute doesn't do anything on its own. After you assign it to a state in a change model, scripts can check whether the attribute is present for a change in that state. For example, a script can allow a feature when the attribute is present and disable it when the attribute is absent.

You assign attributes in the **Attributes** list under each state in the **Model States** related list of a change model. This list appears alongside the state transitions and state field policies for the state.

## Change model attributes in the base system

The base system includes two attributes that already drive change request behavior.

|Label|Name|Description|
|-----|----|-----------|
|Allow CI Modification|`allow_ci_modification`|Determines the states in which you can modify the configuration item and the affected CIs on a change. When the attribute isn't present for a state, the **Configuration item** field is read-only and the options to add or modify affected CIs are removed.|
|Allow Implementation|`allow_implementation`|Determines the states in which you can apply proposed CI changes from a change request.|

## Default behavior when a model has no Allow CI Modification attribute

If you don't assign the Allow CI Modification attribute to any state in a change model, change requests that use the model follow the original change request behavior. The configuration item can be modified only in the New state.

After you assign the attribute to at least one state, the model controls CI modification. The configuration item can be modified only in the states that have the attribute. For example, if you assign the attribute only to the Assess state, the **Configuration item** field is read-only in the New state.

## Example use of change model attributes

Some organizations use a change request to create a configuration item. The CI doesn't exist at the start of the process, so the **Configuration item** field stays empty. After the change passes through the required approvals, the CI is created and added to the change at the end of the process. Assigning the Allow CI Modification attribute to only the final states supports this process.

-   **[Create a change model attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/create-change-model-attribute.md)**  
Create a custom change model attribute that you can assign to states in a change model and check in scripts to control behavior for each state.
-   **[Add an attribute to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/add-attribute-change-model-state.md)**  
Assign a change model attribute to a state in a change model so that scripts can check for the attribute when a change request is in that state.
-   **[Change model attribute API methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/change-model-attribute-apis.md)**  
Use these server-side and client-side methods to check which change model attributes are present for a change request in its current state.

**Parent Topic:**[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/create-a-change-model.md)

