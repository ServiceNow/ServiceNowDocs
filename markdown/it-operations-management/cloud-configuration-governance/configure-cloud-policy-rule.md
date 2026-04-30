---
title: Configure a cloud policy rule
description: A policy rule is a collection of conditions and actions. ​If all conditions evaluate to true, the policy engine performs the actions. If any condition evaluates to false, the policy engine does not perform the actions.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure a cloud policy rule

A policy rule is a collection of conditions and actions. ​If all conditions evaluate to true, the policy engine performs the actions. If any condition evaluates to false, the policy engine does not perform the actions.

## Before you begin

Optional: [Create one or more cloud policy groups](create-cloud-policy-group.md).

Role required: sn\_cmp.cloud\_governor or admin

## About this task

-   A policy can include multiple rules​. You can configure the order that rules are applied.
-   Every rule is executed to completion.​
-   Any rule error stops execution. Exception: Policies that do not specify an operation​.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  On the Rules related list, click **New** and then enter a descriptive **Name** for the rule.

    -   The rule name cannot be the same as the policy name.
    -   The rule name should not start with a number.
4.  Using the base-system condition builder, specify the **Conditions** that must be met for the policy engine to perform the actions.

    The following example rule is applied for a blueprint provision approval policy. The condition evaluates to true if the **OS profile** field on the request form has the value “Windows”.

    ![Configuring a condition to test the requested OS](../image/condition-example-os-profile.png)

<table id="table_bth_qm3_jbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Criteria type\]

</td><td>

Select one of the following options:-   **Request Form**: Base the condition on a property \(attribute\) value in the request form in the Cloud User Portal. You specify which property to test. In the example, the condition tests whether the OS profile field on the request form has the value “Windows.”
-   **User**: Base the condition on a user role or on the group that the user belongs to.

For example, to create a condition that applies when the user belongs to the Marketing group, select:

    -   \[Criteria Type\]: User
    -   \[User Entity\]: Group
    -   \[Relational Operator\]: Equals
    -   \[Group\]: Marketing
 **Note:** You use different criteria to build a condition for policies that are triggered by the `on Lease end` trigger. See the example that appears after the table.

</td></tr><tr><td>

\[Relational Operator\]

</td><td>

Select an appropriate operator.

</td></tr><tr><td>

\[Value\]

</td><td>

Depending on the selected \[Criteria type\], enter or select a value. -   For **Request Form**, enter a value for the attribute.
-   For **User** &gt; **Group**, select a group.
-   For **User** &gt; **Role**, select a role.


</td></tr><tr><td>

\[Logical operator\]

</td><td>

When defining multiple conditions, select a logical operator **OR** or **AND** that specifies the logical relationship with the next condition.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Example

For policies that are triggered by the `on Lease end` trigger, use the base-system date condition builder to configure the condition to test. In addition to the condition, the following example shows the actions that the policy engine performs if the condition is met.

![Condition and actions for a Lease end policy](../image/cloud-policy-rule.png "Condition and actions for a lease end policy")

## What to do next

Create the policy actions that should run when all conditions of the rule evaluate to true.

**Parent Topic:**[Create a cloud policy](create-cloud-policy.md)

