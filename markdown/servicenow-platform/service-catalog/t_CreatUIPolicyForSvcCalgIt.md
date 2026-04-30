---
title: Create a UI policy for catalog items
description: You can apply UI policies for catalog items ordered in the service catalog.The following is an example of how Service Catalog UI policies work.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Service catalog UI policy, Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a UI policy for catalog items

You can apply UI policies for catalog items ordered in the service catalog.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Catalog UI Policies**.

2.  Select **New**.

3.  In the **Applies to** field, select **A Catalog Item**.

4.  Fill in the remaining fields.

<table id="table_gl5_4tk_qq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Select the type of item this UI policy applies to:-   **A Catalog Item**: enables the **Catalog item** field.
-   **A Variable Set**: enables the **Variable set** field.


</td></tr><tr><td>

Catalog Item or Variable Set

</td><td>

Select the catalog item or a variable set this UI policy applies to. The field name and options available depend on the **Applies to**selection.

</td></tr><tr><td>

Short description

</td><td>

Enter a brief description \(example, Out-of-state move\).

</td></tr><tr><td>

Active

</td><td>

Select the check box to enable the UI policy. Clear the check box to disable it.

</td></tr><tr><td class="sub-head" colspan="2">

When to Apply

</td></tr><tr><td>

Catalog Conditions

</td><td>

Create conditions for the UI policy using catalog item variables. The policy is applied if the conditions evaluate to be true. For example, a catalog item of **Schedule a Move** may have a condition of **move\_from &gt; is &gt; San Diego**. The UI policy is applied when an employee schedules a move from San Diego to any other company location.**Note:** The label of a variable associated with a variable set reflects the variable set name. The format is *variable\_set\_name » variable\_name*.

</td></tr><tr><td>

Applies on a Catalog Item view

</td><td>

Select the check box to apply the UI policy to catalog items within the order screen. Available in the requester view.

</td></tr><tr><td>

Applies on Catalog Tasks

</td><td>

Select the check box to apply the UI policy on a Catalog Task form. Available in the fulfiller view. See [VEditor](../concept/service-catalog-variable-editor.md#cat-VEditor).

</td></tr><tr><td>

Applies on Requested Items

</td><td>

Select the check box to apply the UI policy on a Requested Item form. Available in the fulfiller view. See [VEditor](../concept/service-catalog-variable-editor.md#cat-VEditor).

</td></tr><tr><td>

Applies on the Target Record

</td><td>

Select the check box to support the catalog UI policy on a record created for task-extended tables via record producers. See [Default variable editor](../concept/service-catalog-variable-editor.md#cat-default-variable-editor).

</td></tr><tr><td>

On load

</td><td>

Select the check box to apply the UI policy when the form is loaded. Clear the check box to apply the policy only when the form is changed.

</td></tr><tr><td>

Reverse if false

</td><td>

Select the check box to reverse the UI policy if the **Catalog Conditions** statement evaluates to false.

</td></tr><tr><td class="sub-head" colspan="2">

Script

</td></tr><tr><td>

Run scripts

</td><td>

Select the check box to use the **Execute if true** and **Execute if false** scripting fields. Scripts are necessary to apply a UI policy other than **Read Only**, **Mandatory**, or **Visible**. For example, you must create a script to apply a UI policy to a specific role.

</td></tr><tr><td class="sub-head" colspan="2">

Other fields

</td></tr><tr><td>

Order

</td><td>

Enter the sequence in which this UI policy is evaluated if more than one matching UI policy exists. The order is evaluated from the lowest value to the highest value.

</td></tr><tr><td>

Global

</td><td>

This field isn’t used for the service catalog.

</td></tr><tr><td>

Inherit

</td><td>

This field isn’t used for the service catalog.

</td></tr><tr><td class="sub-head" colspan="2">

Catalog UI Policy Actions

</td></tr><tr><td>

Variable name

</td><td>

Select the variable or variable set that belongs to the catalog item. When you apply catalog UI policy actions on a variable set, the actions are applied on all variables within the variable set. If different catalog UI policy actions are applied on a variable or a variable set, the action with the lowest order is considered.

 **Note:**

-   The set value UI policy action isn't applicable for the attachment and masked variables.

Use the **Clear the variable value** option to clear the value for the attachment and masked variables.

-   For multi-row variable set, you can apply a UI policy action on the complete variable set but not on individual variables inside it.
-   The label of variables associated with a variable set reflects the variable set name. The format is *variable\_set\_name » variable\_name*.


</td></tr><tr><td>

Order

</td><td>

Sequence in which the UI policy action is evaluated. The order is evaluated from the lowest value to the highest value. This is also applicable in Service Portal.

</td></tr><tr><td>

Mandatory

</td><td>

Choice list for specifying how the UI policy affects the mandatory state of the field. Choices are:-   Leave alone
-   True
-   False


</td></tr><tr><td>

Visible

</td><td>

Choice list for specifying how the UI policy affects the visible state of the field. Choices are:-   Leave alone
-   True
-   False


</td></tr><tr><td>

Read Only

</td><td>

Choice list for specifying how the UI policy affects the read-only state of the field. Choices are:-   Leave alone
-   True
-   False


</td></tr><tr><td>

Value action

</td><td>

Choice list for specifying whether to set a value for the question, clear the value, or set nothing for the question. Here are the choices.-   Leave alone
-   Set value: Option to set a value for the question in the catalog item.
-   Clear value: Option to clear the variable value.


</td></tr><tr><td>

Value

</td><td>

Enter a value for the question.

 This field appears only when you select **Set value** from the Value action list.

</td></tr><tr><td>

Field message type

</td><td>

Select any of the message types that you want to show for the question.

-   Info
-   Warning
-   Error
 **Note:** If you don’t want any message, select **None**.

</td></tr><tr><td>

Field message

</td><td>

Enter a message that you want to show for the question when a specified condition is met.

 This field appears only when you select a value from the Field message type list.

</td></tr></tbody>
</table>5.  Select **Submit**.

    **Note:** Configure the variable form to display all fields.


**Parent Topic:**[Service catalog UI policy](../concept/c_ServiceCatalogUIPolicy.md)

## Service Catalog UI policy examples

The following is an example of how Service Catalog UI policies work.

The following UI policy makes it mandatory for any department to specify the name of the department if **Department** is selected for the question **Department or group?**.

![Catalog UI policy](../image/CatalogUIPolicyExmple.png "Catalog UI policy")

