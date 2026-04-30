---
title: Configure a blueprint rule
description: Configure a rule that contains actions the system can take on blueprint attributes.Configure the condition on a blueprint form event rule that determines when the actions in the rule can run. Conditions are optional.Configure actions that the system runs when blueprint form attribute actions or event actions are triggered. You can configure actions like making a field mandatory, showing or hiding a field, or automatically populating a field.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Build a Cloud Provisioning blueprint, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure a blueprint rule

Configure a rule that contains actions the system can take on blueprint attributes.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## Procedure

1.  Open a blueprint that has the attribute for which you want to create a rule.

2.  On the **Catalog** tab, click the operation, such as the provision operation, that contains the attribute.

    ![Provision operation](../image/provision-operation-blueprint.png)

3.  In the Variable Sets related list on the Cloud Catalog Item form, click the name of the variable set that contains the variable.

4.  In the Cloud Variables related list on the Variable Set form, click the name of the variable for which you want to crate the rule.

5.  In the Rules related list, click **New** and then fill in the form.

<table id="table_osz_gph_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NameDescription

</td><td>

Enter a name and description.

</td></tr><tr><td>

Order

</td><td>

Enter a number that tells the system which record to evaluate first in relation to others. The record with the lowest number runs first.

</td></tr></tbody>
</table>6.  Right-click the form header and select **Save**.


## Example

This example rule is based on the **CloudAccount** property and contains an action that tells the system to update the list of locations when the user changes the cloud account.

![An example blueprint rule](../image/blueprint-rule.png "Example blueprint rule")

## What to do next

Configure an optional [condition](configure-a-blueprint-rule.md#) and a mandatory [action](configure-a-blueprint-rule.md#).

**Parent Topic:**[Build a Cloud Provisioning blueprint](create-blueprint-cmp.md)

**Related topics**  


[Add a resource operation to the execution plan](add-resource-operation-cmp.md)

[Execute blueprint operations in parallel](execute-blueprint-operations-parallel.md)

[Blueprint attributes](../reference/blueprint-attributes.md)

## Configure a blueprint rule condition

Configure the condition on a blueprint form event rule that determines when the actions in the rule can run. Conditions are optional.

### Before you begin

Role required: sn\_cmp.cloud\_service\_designer

### Procedure

1.  Open a [rule for a variable](configure-a-blueprint-rule.md#) on a blueprint.

2.  On the Conditions related list, click **New**.

3.  Fill out the form fields \(see table\).

<table id="table_k4k_chk_wz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operand

</td><td>

Enter the property against which you can perform the condiontal evaluation. For example, if your blueprint has a property which holds the value of a datacenter, enter the property name here.

</td></tr><tr><td>

Operator

</td><td>

Select an operator that evaluates the operand.

</td></tr><tr><td>

Value

</td><td>

Enter a value that the evaluated event rule must match.

</td></tr><tr><td>

Condition Type

</td><td>

If you configure multiple conditions, select the logical operator that determines how the system evaluates the condition in relation to the next condition \(the next condition is determined by the **Order** field\):

-   **AND**: this condition the next condition must meet the criteria before the policy is eligible for execution.
-   **OR**: this condition or the next condition that matches the criteria can allow the policy to be eligible for execution.
If you do not select an option, **AND** is used by default.

</td></tr><tr><td>

Order

</td><td>

Enter a number that tells the system which record to evaluate first in relation to others. The record with the lowest number runs first.

</td></tr><tr><td>

Status

</td><td>

Keep the status active to have the system process the condition. Change the status to inactive when you do not want the system to process the condition.

</td></tr></tbody>
</table>4.  Click **Submit**.


### Example

This example condition applies when the user selects the AWS Datacenter for the Logical\_Datacenter property, which is a field on the catalog item form:

![Example blueprint condition](../image/blueprint-condition.png "Example blueprint condition")

### What to do next

[Configure a blueprint action](configure-a-blueprint-rule.md#).

## Configure a blueprint action

Configure actions that the system runs when blueprint form attribute actions or event actions are triggered. You can configure actions like making a field mandatory, showing or hiding a field, or automatically populating a field.

### Before you begin

Role required: sn\_cmp.cloud\_service\_designer

### Procedure

1.  Open a rule for a property or an event on a blueprint.

2.  On the **Actions** related list, click **New** and then fill in the form.

<table id="table_nls_lrk_wz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name.

</td></tr><tr><td>

Action Type

</td><td>

Select an action type: -   **Reload**:
-   **Show**:
-   **Hide**:
-   **MakeMandatory**:
-   **MakeNonMandatory**:
-   **TriggerChangeEvent**:
-   **SetValue**:


</td></tr><tr><td>

Datasource

</td><td>

Select an action type: -   **Reload Cloud Account**:
-   **Reload Cloud Location**:
-   **Check Quota**:
-   **Reload Resource Profile**:
-   **Reload From Profile**:


</td></tr><tr><td>

Target Field

</td><td>

Enter the name of the field on the form that the action applies to. For example, if you selected **TriggerChangeEvent** for the action type, the value of the field changes when something changes on the form, as specified in the [blueprint rule](configure-a-blueprint-rule.md#).

</td></tr><tr><td>

Value

</td><td>

Enter an optional value that you want to assign to the target field. For example, if you selected **SetValue** for the **Action Type** field and you want to update the **Resource Group Name**, you can use the value `${ResourceGroup}`, which pulls the names of the resource groups from the blueprint.

</td></tr><tr><td>

Order

</td><td>

Enter a number that tells the system which record to evaluate first in relation to others. The record with the lowest number runs first.

</td></tr></tbody>
</table>3.  Right-click the header and select **Save**.

4.  Enter a **Key** and **Value** in the KeyValues related list.

    The value in the **Value** field is applied to the attribute in the **Key** field.

5.  Create as many actions as necessary.


### Example

This example action applies to the [blueprint rule example](configure-a-blueprint-rule.md#), which is based on the CloudAccount attribute. The action tells the system to update the list of locations when the user changes the cloud account.

![Configuring a blueprint action](../image/blueprint-action.png "Example blueprint action")

### What to do next

[Publish a blueprint as a cloud catalog item](catalog-item-from-blueprint-cmp.md).

