---
title: Change Models properties
description: Configure the Change Models properties to access the Change models capabilities when creating a Change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/change-management/change-models-properties.html
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Change models, Exploring Change Management, Change Management, IT Service Management]
---

# Change Models properties

Configure the Change Models properties to access the Change models capabilities when creating a Change request.

The following properties enable you to access the Change Models features. For upgrade users, these properties are set to **true**.

**Important:** A wildcard search for `*change_model` in `sys_properties.list` may return additional properties depending on the installed plugins, such as `com.snc.change_management.change_model.default_read_roles`, which controls read access to change model records. Confirm the value of any role-based property before changing it. For the roles referenced, see [Components installed with ITSM Roles - Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/installed-with-cm-itsm-roles.md).

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

</td></tr><tr><td>

com.snc.change\_management.change\_model.default\_read\_roles

</td><td>

Comma-separated roles that have read access to change model records. Use this property to restrict who can view change model definitions.

</td></tr></tbody>
</table>**Note:** If type compatibility is set to false, and change type does not match with a corresponding change model, the change model is marked as Legacy.

**Parent Topic:**[Change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/change-models.md)

