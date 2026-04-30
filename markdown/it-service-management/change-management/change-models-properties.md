---
title: Change Models properties
description: Configure the Change Models properties to access the Change models capabilities when creating a Change request.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Change models, Exploring Change Management, Change Management, IT Service Management]
---

# Change Models properties

Configure the Change Models properties to access the Change models capabilities when creating a Change request.

The following properties enable you to access the Change Models features. For upgrade users, these properties are set to **true**.

Enter `sys_properties.list` in the navigation filter and enter `*change_model` in the Search panel to view and edit the properties.

|Property|Description|
|--------|-----------|
|com.snc.change\_management.change\_model.hide|Hides the Change models feature when the **com.snc.change\_management.change\_model.type\_compatibility** property is enabled. When creating a new change, you do not have the option to choose a model, and the **Model** field is not available on the Change request form.|
|com.snc.change\_management.change\_model.manage\_workflow|Enables Workflow management support for ChangeRequest API if the **com.snc.change\_management.state\_model** plugin is installed. This will call the 'deleteDefaultWorkflowContext' method to be called on specific state and type changes.|
|com.snc.change\_management.change\_model.type\_compatibility|Enables Change Type Compatibility for Change models if the **com.snc.change\_management.state\_model** plugin is installed. When true allows changes to be created with both the type based workflow and Change models.|

**Parent Topic:**[Change models](../concept/change-models.md)

