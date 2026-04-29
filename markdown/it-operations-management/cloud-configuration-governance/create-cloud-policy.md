---
title: Create a cloud policy
description: A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort subflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a cloud policy

A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort subflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.

## Before you begin

-   Optional: [Create one or more cloud policy groups](create-cloud-policy-group-1.md).
-   Role required: sn\_cmp.cloud\_governor or admin

## About this task

This procedure describes every policy type except approval policies \(on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation\). See [Create a cloud approval policy](create-cloud-approval-policy.md) for instructions on creating a policy with an approval trigger.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Click **New** and then fill in the form.

    ![Policy form](../image/new-cloud-policy.png "Example policy form")

<table id="table_zk1_ctq_fz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy Name

</td><td>

A descriptive name that includes the word `Policy`. Do not start the name with a number.

</td></tr><tr><td>

Description

</td><td>

A description of the intent of the policy.

</td></tr><tr><td>

Policy Group

</td><td>

A policy group to which the policy belongs.

</td></tr><tr><td>

Policy Trigger

</td><td>

A trigger that specifies when the policy should be applied. For example, the **on Lease end** trigger applies the policy when the lease for a stack ends. See [Triggers for cloud policies](../reference/policy-triggers-cloud-mgt.md).

</td></tr><tr><td>

Resource Block\[appears when the on Resource Operation trigger is selected\]

</td><td>

The resource block that the policy applies to.

</td></tr><tr><td>

Operation\[appears when the on Blueprint provision, on Blueprint provision \(approval\) or on Resource Operation trigger is selected\]

</td><td>

Select the operation that the policy applies to. For example, a policy can apply to the Deprovision operation only or to all operations on the blueprint or catalog item.**Note:** If no operation is specified, then the policy applies for every operation. This condition can decrease performance.

 -   **All**: Any operation executes.
-   **Start**: The resource starts.
-   **Stop**: The resource stops.
-   **Provision**: The resource is provisioned.
-   **Deprovision**: The resource is no longer available to users.
-   **Execute Script**: A script runs on the resource.


</td></tr><tr><td>

Moment\[appears when the on Resource Operation trigger is selected\]

</td><td>

Specify when the policy should be enforced:-   **Pre-operation**: Before the specified operation starts.
-   **Post-operation**: After the specified operation finishes.
 **Note:** If you are integrating with Infoblox, use **Pre-operation** for a vSphere virtual machine. Use **Post-operation** for AWS and Azure clouds because AWS and Azure control the allocation of IP addresses. You can register the IP address that is provided with Infoblox.

</td></tr><tr><td>

Catalog item\[appears when an on Catalog item launch, on Catalog item request start, or on Catalog item request end trigger is selected\]

</td><td>

Select the catalog item that the policy applies to.

</td></tr><tr><td>

Start Date / End Date

</td><td>

Specify the start date when the policy should be considered and the end date when the policy should no longer be considered.

</td></tr><tr><td>

Order of Execution

</td><td>

Specify a number that represents the order in which the policy is applied. A policy with a lower number runs before a policy with a higher number. For example, a policy with **Order** of **100** runs before a policy with an **Order** of **200**.

 **Note:** The **Order of Execution** property does not apply for on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation policies. See [Create a cloud approval policy](create-cloud-approval-policy.md) for details.

</td></tr><tr><td>

Status

</td><td>

-   **Published** policies are enforced. You cannot edit a policy in the **Published** state. To edit a policy that is in the **Published** state, click **Draft** on the form header.
-   You can edit **Draft** policies. **Draft** policies are not enforced. To enforce a policy, click **Publish** on the form header.


</td></tr></tbody>
</table>3.  Right-click in the header and select **Save**.


## What to do next

[Configure a cloud policy rule](configure-cloud-policy-rule.md) for the policy.

-   **[Configure a cloud policy rule](configure-cloud-policy-rule.md)**  
A policy rule is a collection of conditions and actions. ​If all conditions evaluate to true, the policy engine performs the actions. If any condition evaluates to false, the policy engine does not perform the actions.
-   **[Using expressions in Cloud Provisioning and Governance](../reference/expressions-cloud-mgt.md)**  
Expressions in policy actions can set or override values. Expressions in blueprints can access attributes of resources and can map values to request form fields. Expressions are available in resource blocks, blueprints, policies, and anywhere that Cloud Provisioning and Governance allows scripts.
-   **[Create an action for an 'on Blueprint provision' policy](create-action-on-bp-provision.md)**  
The on Blueprint provision trigger fires after execution of on Catalog item request start policies. A policy that is triggered by the on Blueprint provision trigger can run a script, override a user-requested attribute value, or abort and send a message about the provision operation.
-   **[Create an action for an approval policy](create-action-on-approval.md)**  
A policy that is triggered by one of the approval triggers can start approval subflows. The approval triggers are \(on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation.
-   **[Create an action for an 'on Catalog item launch' policy](create-action-on-cat-item-launch.md)**  
The on Catalog item launch trigger fires when an order form \(stack request form\) is launched for a catalog item. A policy that is triggered by the on Catalog item launch trigger can run a script or override a user-requested value \(text values only\).
-   **[Create an action for an 'on Catalog item request start/end' policy](create-action-on-cat-item-request.md)**  
The on Catalog item request start trigger fires after the user opens a request form. The on Catalog item request end trigger fires after a user submits a request form. A policy that is triggered by the on Catalog item request start or on Catalog item request end trigger can run a script or execute a subflow.
-   **[Create an action for an 'on Lease end' policy](create-action-on-lease-end.md)**  
A policy that is triggered by the on Lease end trigger can send a notification or perform a Start, Stop, or Deprovision life cycle operation.
-   **[Create an action for an 'on Resource operation' policy](create-action-on-resource-op.md)**  
The on Resource operation trigger fires during the Orchestration process when a user performs a Start, Stop, or Deprovision life cycle operation on a specific resource. A policy that is triggered by the on Resource operation trigger can override a user-requested attribute value, run a script, call a Cloud API, or perform an IP address management operation.
-   **[Create an action for an 'on Resource operation launch' policy](create-action-on-resrce-op-launch.md)**  
The on Resource operation launch trigger fires before the catalog for a resource operation is loaded from the Cloud User Portal. A policy that is triggered by the on Resource operation launch trigger can run a script or can override a user-requested value \(text values only\).
-   **[Create an action for an 'on Resource operation request start/end' policy](create-action-on-resrce-op-reqst.md)**  
A policy that is triggered by the on Resource operation request start or on Resource operation request end trigger can run a script or override a user-requested attribute value.
-   **[Create an action for an 'on Resource Limit exceeded' policy](create-action-on-resource-limits-exceeded.md)**  
Set the **on Resource limits exceeded** policy to automatically run approval subflows or send notifications when an order form is submitted for a template-based catalog item that exceeds the defined resource limit or quota values.
-   **[Create an action for an 'on Task Remediation' policy](create-action-on-remediation.md)**  
The on Task remediation trigger fires when a user resubmits a failed request. A policy that is triggered by the on Task Remediation trigger can start approval subflows.
-   **[Create a policy action script](create-policy-script.md)**  
Use policy action scripts to get, update, or set values in cloud requests.
-   **[Example policy action script that tags resources](add-tag-for-policy.md)**  
Your instance tracks tagged resources for billing and reporting. Policy action scripts can add and modify resource tags. This example tags a storage volume resource.

**Parent Topic:**[Policies for Cloud Provisioning](../concept/cloud-policy.md)

