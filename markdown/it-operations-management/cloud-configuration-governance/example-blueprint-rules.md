---
title: Cloud catalog form configuration examples
description: Several examples are provided to help you understand how to manipulate Cloud catalog order forms. These example cover blueprint rules, blueprint variables, and blueprint form UI groups.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud catalog form configuration examples

Several examples are provided to help you understand how to manipulate Cloud catalog order forms. These example cover blueprint rules, blueprint variables, and blueprint form UI groups.

<table id="table_nhb_qzn_p2b"><thead><tr><th>

Example

</th><th>

Goal

</th><th>

Blueprint components used

</th></tr></thead><tbody><tr><td>

[Populate the location based on the cloud account](../task/analyze-default-blueprint-rules.md)

</td><td>

Use existing blueprint rules to illustrate how the Location field is populated based on the Cloud Account that the user selects.

</td><td>

This example illustrates rules.

</td></tr><tr><td>

[Remove a field from a cloud catalog form](../task/remove-mandatory-field-example.md)

</td><td>

Hide the Cost Center field on the catalog form when the catalog requester belongs to the Database group.

</td><td>

This example illustrates:-   Rules
-   Resource pools

</td></tr><tr><td>

[Populate stack name with a script](../task/populate-stack-name-example.md)

</td><td>

Give the catalog requester a pre-defined stack name that includes the ID of the catalog requester. The field remains editable to the user can change it if necessary.

</td><td>

This example illustrates:-   Rules
-   Resource pools
-   Scripted values

</td></tr><tr><td>

[Add fields to a cloud catalog item order form](../task/add-fields-control-order-blueprint.md)

</td><td>

Create a catalog variable and property, and use it to publish a new filed on a form.

</td><td>

This example illustrates:-   Catalog variables
-   Field order
-   Rules
-   Resource pools
-   Scripted values

</td></tr><tr><td>

[Set default values for a cloud catalog form fields](../task/set-value-reference-or-pool.md)

</td><td>

Set a default value on a property and on a blueprint rule.

</td><td>

This example illustrates:-   Default variables
-   Rules

</td></tr><tr><td>

[Add a UI group with additional fields](../task/configure-ui-group.md)

</td><td>

Group catalog form fields into tabs to better organize the form and guide the user from one set of settings to another.

</td><td>

This example illustrates UI groups \(tabs\).

</td></tr></tbody>
</table>-   **[Populate the location based on the cloud account](../task/analyze-default-blueprint-rules.md)**  
This example walks you through an existing set of blueprint rules that Cloud Provisioning and Governance provides by default.
-   **[Remove a field from a cloud catalog form](../task/remove-mandatory-field-example.md)**  
Remove a field from the Cloud Provisioning and Governance catalog form when the user belongs to a specific group.
-   **[Populate stack name with a script](../task/populate-stack-name-example.md)**  
This example illustrates how to populate the name of the stack that a user requests from the Cloud Provisioning and Governance catalog by utilizing the user's ID. The example uses a script include that you can call from a blueprint rule action.
-   **[Set default values for a cloud catalog form fields](../task/set-value-reference-or-pool.md)**  
You can set default values for all users or you can populate fields with default values based on conditions. This example shows you how to set a default schedule profile and business service.

**Parent Topic:**[Form configuration with blueprints](blueprint-form-configuration.md)

