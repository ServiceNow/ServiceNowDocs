---
title: Change Models properties
description: Configure the Change Models properties to access the Change models capabilities when creating a Change request.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Change models, Explore, Change Management, IT Service Management]
---

# Change Models properties

Configure the Change Models properties to access the Change models capabilities when creating a Change request.

The following properties enable you to access the Change Models features. For upgrade users, these properties are set to **true**.

Enter `sys_properties.list` in the navigation filter and enter `*change_model` in the Search panel to view and edit the properties.

<table id="table_szt_rh5_znb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.change\_management.change\_model.hide

</td><td>

Hides the Change models feature when the **com.snc.change\_management.change\_model.type\_compatibility** property is enabled. When creating a new change, you do not have the option to choose a model, and the **Model** field is not available on the Change request form.

</td></tr><tr><td>

com.snc.change\_management.change\_model.manage\_workflow

</td><td>

Enables Workflow management support for ChangeRequest API if the **com.snc.change\_management.state\_model** plugin is installed. This will call the 'deleteDefaultWorkflowContext' method to be called on specific state and type changes.

</td></tr><tr><td>

com.snc.change\_management.change\_model.type\_compatibility

</td><td>

Determine what kind of change requests \(type or model-based\) are created. Enables Change Type Compatibility for Change models if the **com.snc.change\_management.state\_model** plugin is installed. When set to true, the property allows changes to be created with both the type based workflow and Change models.**Note:** The default value of this property is False. When set to false, change request will be created only using change model.

</td></tr></tbody>
</table>**Note:** If type compatibility is set to false, and change type does not match with a corresponding change model, the change model is marked as Legacy.

**Parent Topic:**[Change models](../concept/change-models.md)

