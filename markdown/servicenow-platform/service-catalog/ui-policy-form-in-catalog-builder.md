---
title: UI policy form in Catalog Builder
description: Refer to the fields and their descriptions on the UI Policy form in Catalog Builder.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Edit a catalog item in Catalog Builder, Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# UI policy form in Catalog Builder

Refer to the fields and their descriptions on the UI Policy form in Catalog Builder.

<table id="table_pjv_lr3_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Active

</td><td>

Enable this option to activate and apply the UI policy or dynamic behavior to the catalog item.

</td></tr><tr><td>

Applies to

</td><td>

Selected by default; this is the name of your catalog item that this UI policy applies to. It’s a read-only field.

</td></tr><tr><td>

Short description

</td><td>

Specify the purpose of this behavior.

</td></tr><tr><td>

Order

</td><td>

Enter the sequence in which this UI policy is evaluated if more than one matching UI policy exists. The order is evaluated from the lowest value to the highest value.

</td></tr><tr><td>

On Load

</td><td>

Select the check box to apply the UI policy when the form is loaded. Clear the check box to apply the policy only when the form is changed.

</td></tr><tr><td>

Reverse if false

</td><td>

Select the check box to reverse the UI policy if the catalog conditions statement evaluates to false.

</td></tr><tr><td colspan="2">

Conditions

</td></tr><tr><td>

Conditions

</td><td>

Define the conditions that must be met to trigger and run this behavior.

</td></tr><tr><td colspan="2">

Actions

</td></tr><tr><td>

Add new action

</td><td>

Configure field behavior for the selected question like mandatory, hidden, read-only, value changes, and messages.

</td></tr><tr><td>

Variable name

</td><td>

Question affected when the condition is met.

</td></tr><tr><td>

Order

</td><td>

Sequence in which the UI policy action is evaluated. The order is evaluated from the lowest value to the highest value.

</td></tr><tr><td>

Mandatory

</td><td>

Define if the field is required when the condition is met. The choices are:

-   Leave alone
-   True
-   False

</td></tr><tr><td>

Read only

</td><td>

Set the field to read-only when the condition is met. The choices are:

-   Leave alone
-   True
-   False

</td></tr><tr><td>

Visible

</td><td>

Set to show or hide the field when the condition is met. The choices are:

-   Leave alone
-   Set value
-   Clear value

</td></tr><tr><td>

Field message type

</td><td>

Show an info, warning, or error message. Choices are:

-   None
-   Info
-   Warning
-   Error

</td></tr><tr><td colspan="2">

Scripts

</td></tr><tr><td>

Run scripts

</td><td>

Select the check box to use the execute scripting fields. Scripts are necessary to apply a UI policy other than **Read Only**, **Mandatory**, or **Visible**. For example, you must create a script to apply a UI policy to a specific role.

</td></tr><tr><td>

UI Type

</td><td>

Appears if you select the Run scripts check box. Choose the UI type from the choices, where this script will be applied.

-   Desktop
-   Mobile/Service Portal
-   All

</td></tr><tr><td>

Execute if true

</td><td>

Use this script to define behavior when the conditions of this policy are met. Appears if you select the **Run scripts** check box.

</td></tr><tr><td>

Execute if false

</td><td>

Use this script to define behavior when the conditions of this policy are not met. Appears if you select the **Run scripts** check box.

</td></tr><tr><td colspan="2">

Applies to

</td></tr><tr><td>

Applies when the item is being requested

</td><td>

Select the check box so that the UI policy applies when the item is being requested.

</td></tr><tr><td>

Applies while viewing the catalog tasks after the request is submitted

</td><td>

Select the check box so that the UI policy applies while viewing the catalog tasks after the request is submitted.

</td></tr><tr><td>

Applies while viewing the requested item record after the request is submitted

</td><td>

Select the check box so that the UI policy applies while viewing the requested item record after the request is submitted.

</td></tr></tbody>
</table>**Parent Topic:**[Edit a catalog item in Catalog Builder](edit-cat-item-cat-builder.md)

**Related topics**  


[Create UI policies in Catalog Builder](create-ui-policies-in-catalog-builder.md)

