---
title: Create a cloud policy
description: A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort workflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a cloud policy

A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort workflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.

## Before you begin

-   Optional: [Create one or more cloud policy groups](create-cloud-policy-group-1.md).
-   Role required: sn\_cmp.cloud\_governor or admin

## About this task

This procedure describes every policy type except approval policies \(on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation\). See [Create a cloud approval policy](create-cloud-approval-policy-1.md) for instructions on creating a policy with an approval trigger.

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

A trigger that specifies when the policy should be applied. For example, the **on Lease end** trigger applies the policy when the lease for a stack ends. See [Triggers for cloud policies](../reference/policy-triggers-cloud-mgt-1.md).

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

 **Note:** The **Order of Execution** property does not apply for on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation policies. See [Create a cloud approval policy](create-cloud-approval-policy-1.md) for details.

</td></tr><tr><td>

Status

</td><td>

-   **Published** policies are enforced. You cannot edit a policy in the **Published** state. To edit a policy that is in the **Published** state, click **Draft** on the form header.
-   You can edit **Draft** policies. **Draft** policies are not enforced. To enforce a policy, click **Publish** on the form header.


</td></tr></tbody>
</table>3.  Right-click in the header and select **Save**.


## What to do next

[Configure a cloud policy rule](configure-cloud-policy-rule-1.md) for the policy.

