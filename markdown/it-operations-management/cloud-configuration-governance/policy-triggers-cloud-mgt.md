---
title: Triggers for cloud policies
description: Triggers are events that set the policy engine in motion. For example, the on Catalog item request end trigger fires after a user submits a request form. When the trigger for a policy fires, the policy engine tests the conditions specified in the policy rule and performs the actions specified in the rule, if the conditions are met.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Triggers for cloud policies

Triggers are events that set the policy engine in motion. For example, the on Catalog item request end trigger fires after a user submits a request form. When the trigger for a policy fires, the policy engine tests the conditions specified in the policy rule and performs the actions specified in the rule, if the conditions are met.

## About triggers

-   You typically refer to a policy by the name of the trigger for the policy. For example, you might refer to a policy that is triggered by the on Lease end trigger as a "Lease end policy."
-   Triggers are often based on user requests and the operations \(start, stop, provision, or de-provision\) that can run on a blueprint, a catalog item, a resource, or a stack. Some trigger types do not specify a cloud operation. For example, the on Lease End trigger fires independently of any operation.
-   To optimize performance, limit the number of policies with general triggers like the on Catalog item triggers.
-   A trigger that does not specify a target \(a blueprint, catalog item, stack, or resource\) is always executed. To optimize performance, therefore, minimize the use of such policies.

**Important:** Blueprints are deprecated. The trigger descriptions following the time-line schema below, are applicable for creating cloud template based catalogs as well.

![Provisioning trigger time line](../image/provision-trigger-timeline.png "Provisioning trigger time-line")

## Policy triggers

<table id="table_kml_4lg_5fb"><thead><tr><th>

Trigger name and actions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

on Blueprint provision

 Actions:

 -   Execute a script
-   Property override
-   Abort process

</td><td>

The on Blueprint provision trigger fires after execution of on Catalog item request start policies. A policy that is triggered by the on Blueprint provision trigger can run a script, override a user-requested attribute value, or abort and send a message about the provision operation. Use this trigger to override a value that the user enters. For example, when a user chooses a value for an attribute like the stack name, a policy with this trigger can change the stack name. In addition, another action can change the name again when the user finally provisions the resource.

 The user does not see the final value on the catalog item form because the change is made at provision time.

 [Create an action for an 'on Blueprint provision' policy](../task/create-action-on-bp-provision-1.md)

</td></tr><tr><td>

Approval triggers

 -   **on Stack operation \(approval\)**: Triggered during any stack operation on the Cloud User Portal.
-   **on Stack resource operation \(approval\)**: Triggered during any resource operation \(start, stop, provision, and so on\) on the Cloud User Portal.
-   **on Task remediation**: Triggered when a user resubmits a failed request.

 Actions:

 -   ServiceNow Approval
-   Custom Approval

</td><td>

A cloud approval policy specifies the users who must approve a specified cloud activity before the activity can proceed. Approvers can include the manager of the user making a request, a specified user or group, or users with a specified role. You can specify multiple approvers. Approvals occur in the order that you specify. A policy that is triggered by one of the approval triggers can start approval workflows. The targeted approval policies complement the base-system approval operations.

 **Note:** The approval process is performed after properties are set because property values that were overridden could change costs.

 on Blueprint provision \(approval\) is applied before the blueprint is provisioned. Because the provisioning process can alter request data \(and possibly change costs\), approval processes run after the blueprint is provisioned.

 Use on Stack operation \(approval\) to run an approval workflow when an operation is performed on a stack. By default, a change request is generated when an operation is performed on a stack, but it does not require an approval. This trigger can launch a mandatory approval.

 Use on Stack resource operation \(approval\) to run an approval workflow when an operation is performed on a single resource that is part of a stack. By default, a change request is generated when an operation is performed on a stack, but it does not require an approval. This trigger can launch a mandatory approval.

 A policy that is triggered by the on Task Remediation trigger can start approval workflows.

 [Create an action for an 'approval' policy](../task/create-action-on-approval-1.md)

</td></tr><tr><td>

on Catalog item launch

 Actions:

 -   Execute a script
-   Property override

</td><td>

The on Catalog item launch trigger fires when an order form \(stack request form\) is launched for a catalog item. A policy that is triggered by the on Catalog item launch trigger can run a script or override a user-requested value \(text values only\). Use this trigger to control what the user sees in the form when it first opens in the Cloud User Portal. For example, you can override a default value that first appears to the user. The user can see this value on the catalog item form.

 When both a policy rule and a form rule overwrite a value, the value in the form rule is used.

 [Create an action for an 'on Catalog item launch' policy](../task/create-action-on-cat-item-launch-1.md)

</td></tr><tr><td>

on Catalog item request start

 Actions:

 -   Execute a script
-   Execute a workflow

</td><td>

The on Catalog item request start trigger fires after the user opens a request form. A policy that is triggered by the on Catalog item request start or on Catalog item request end trigger can run a script or execute a workflow.

 You can use this trigger to run a custom script or workflow to fulfill enterprise processes like custom approval before the catalog item request is processed.​

 [Create an action for an 'on Catalog item request start/end' policy](../task/create-action-on-cat-item-request-1.md)

</td></tr><tr><td>

on Catalog item request end

 Actions:

 -   Execute a script
-   Execute a workflow

</td><td>

The on Catalog item request end trigger fires after a user submits a request form. A policy that is triggered by the on Catalog item request start or on Catalog item request end trigger can run a script or execute a workflow.

 Use this trigger to launch a workflow after a catalog item request is processed. Consider this trigger a post-provisioning step. For example, you could launch a workflow to install MySQL on the provisioned resource.

 [Create an action for an 'on Catalog item request start/end' policy](../task/create-action-on-cat-item-request-1.md)

</td></tr><tr><td>

on Lease end

 Actions:

 -   Run an Operation
-   Send a Notification

</td><td>

A policy that is triggered by the on Lease end trigger can send a notification or perform a Start, Stop, or Deprovision life cycle operation. [Create an action for an 'on Lease end' policy](../task/create-action-on-lease-end-1.md)

</td></tr><tr><td>

on Resource operation launch

 Actions:

 -   Execute a script
-   Property override

</td><td>

The on Resource operation launch trigger fires before the catalog for a resource operation is loaded from the Cloud User Portal. A policy that is triggered by the on Resource operation launch trigger can run a script or can override a user-requested value \(text values only\). When both a policy rule and a form rule overwrite a value, the value in the form rule is used.

 [Create an action for an 'on Resource operation launch' policy](../task/create-action-on-resrce-op-launch-1.md)

</td></tr><tr><td>

on Resource operation request start

 Actions:

 -   Execute a script
-   Execute a workflow

</td><td>

The on Resource operation request start trigger fires after a user submits a resource operation request \(Start, Stop, Deprovision\). A policy that is triggered by the on Resource operation request start or on Resource operation request end trigger can run a script or override a user-requested attribute value.

 [Create an action for an 'on Resource operation request start/end' policy](../task/create-action-on-resrce-op-reqst-1.md)

</td></tr><tr><td>

on Resource operation request end

 Actions:

 -   Execute a script
-   Execute a workflow

</td><td>

The on Resource operation request end trigger fires before completion of a life cycle operation on a resource \(Start, Stop, Deprovision\). A policy that is triggered by the on Resource operation request start or on Resource operation request end trigger can run a script or override a user-requested attribute value.

 [Create an action for an 'on Resource operation request start/end' policy](../task/create-action-on-resrce-op-reqst-1.md)

</td></tr><tr><td>

on Resource operation

 Actions:

 -   Property override
-   Execute a script
-   Call Cloud API
-   IP Address Management

</td><td>

The on Resource operation trigger fires during the Orchestration process when a user performs a Start, Stop, or Deprovision life cycle operation on a specific resource. A policy that is triggered by the on Resource operation trigger can override a user-requested attribute value, run a script, call a Cloud API, or perform an IP address management operation. [Create an action for an 'on Resource operation' policy](../task/create-action-on-resource-op-1.md)

</td></tr></tbody>
</table>**Parent Topic:**[Policies for Cloud Provisioning](../concept/cloud-policy.md)

