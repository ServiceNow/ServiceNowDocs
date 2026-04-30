---
title: Policies for Cloud Provisioning
description: A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort workflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
keywords: [order of execution]
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Policies for Cloud Provisioning

A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort workflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.

## A user requests a stack that triggers an approval policy

1.  On the Cloud User Portal, a user submits a request to provision a particular blueprint. The process of provisioning the blueprint is the trigger that causes the policy engine to apply an approval policy. A cloud approval policy specifies the users who must approve a specified cloud activity before the activity can proceed.
2.  The policy engine determines that the request meets the condition specified in the rule for the policy. In this example, the condition evaluates to true whenever a particular blueprint is being provisioned.
3.  Because the condition is met, the policy engine performs the action that is also specified in the rule. In this example, the action is to create an approval action for the manager.
4.  While the approver \(the manager\) reviews the approval request, the user sees a "waiting for approval" status message on the Cloud User Portal.
5.  After the manager approves, the blueprint is provisioned.

![User waiting for approval](../image/user-awaiting-approval.png "User waiting for approval")

**Note:** You cannot invoke flows while adding a resource operation step. This is a known limitation.

## About policy triggers

Triggers are events that set the policy engine in motion. For example, the on Catalog item request end trigger fires after a user submits a request form. When you think about defining a policy, you might first consider how the policy will be triggered. Examples:

-   A user requests a Stop operation on a virtual server \(the on Stack resource operation trigger fires\)
-   A resource reaches the end of its lease \(the on Lease End trigger fires\)
-   A user requests a particular stack \(the on Blueprint provision trigger fires\)

You typically refer to a policy by the name of the trigger for the policy. For example, you might refer to a policy that is triggered by the on Lease end trigger as a "Lease end policy." For more detail on the types of trigger that you can implement, see [Triggers for cloud policies](../reference/policy-triggers-cloud-mgt.md).

## How policies work

For each policy, you typically configure a trigger that starts the policy engine. The policy engine enforces the policy by running all rules that are defined for the policy. A policy rule is a collection of conditions and actions. ​If all conditions evaluate to true, the policy engine performs the actions. If any condition evaluates to false, the policy engine does not perform the actions.

-   Some policy types apply only to particular types of cloud operation, like start, stop, provision, or deprovision, or to a particular target, like ‘on blueprint123 provision operation’ or ‘on catalog item ABC launch’​.
-   You can configure a policy that does not specify a target, for example, ‘on any blueprint provision operation’ or ‘on any catalog item launch’​. Errors on policies that apply to any object are ignored.
-   If multiple policies apply, you can specify the order that the policies are applied \(with an exception that is described in a following section\).
-   Policies can work with dynamic forms to allow you to show or hide form fields from end users. Users see only information that you decide they need for them to understand and complete their tasks.

## Policy groups

A cloud policy group is a container for related policies. Consider grouping policies that are often used together or should be considered together. Grouping policies can help you to apply policies consistently across your organization.

## Order of execution when multiple policies apply

Order of execution when multiple "approval" policies apply:

When multiple "approval" policies apply, the policies are applied in the following order. \(The approval policies are on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation\):

1.  Only the first successful approval policy is applied and no other approval policies are applied.
2.  If the applied approval policy has multiple rules, only the first successful rule is used.
3.  If a rule has multiple actions, only the first successful action is performed.
4.  If the applied approval policy includes both a custom approval and a Service Now approval, only the custom approval process is performed.

Order of execution for all other policy types:

-   Policies are applied in the order that is specified by the **Order of Execution** property setting.
-   If multiple policies have the same **Order of Execution** setting, then order is not guaranteed.

## About operations in policies

Triggers are often based on user requests and the operations \(start, stop, provision, or de-provision\) that can run on a blueprint, a catalog item, a resource, or a stack. Some trigger types do not specify a cloud operation. For example, the on Lease End trigger fires independently of any operation.

## About policy rules

A policy rule is a collection of conditions and actions. ​If all conditions evaluate to true, the policy engine performs the actions. If any condition evaluates to false, the policy engine does not perform the actions.

-   Conditions: Conditions can consider request form data, resource activity, or user activity. Examples:
    -   Is the size of the requested CPU greater than 32?
    -   Is this a Stop operation?
    -   Is the lease for this resource ending in the next 7 days?
-   Actions: If all conditions evaluate to true, the policy engine runs the actions that the rule specifies. Expressions in policy actions can set or override values. Examples:
    -   Override the value that the user specified by changing the CPU size to 16 and then start the approval process. \(because the condition was met that the requested CPU is greater than 32\).
    -   Create an approval task for the manager. \(because the condition was met that a Stop operation was requested\).
    -   Send notifications to every user in the ABC group. \(because the condition was met that the lease ends in 7 days\).

## Policy action scripts

-   Use policy action scripts to get, update, or set values in cloud requests.
-   Your instance tracks tagged resources for billing and reporting. Policy action scripts can add and modify resource tags.

-   **[Cloud policy example](../task/policy-walkthrough.md)**  
A base system cloud policy, Lease End ServiceNow, uses the on Lease end trigger that fires when a virtual resource is near the lease end date. If the conditions in the policy rule are met, the policy engine sends a notification to the owner of the resource and performs operations on the resource.
-   **[Triggers for cloud policies](../reference/policy-triggers-cloud-mgt.md)**  
Triggers are events that set the policy engine in motion. For example, the on Catalog item request end trigger fires after a user submits a request form. When the trigger for a policy fires, the policy engine tests the conditions specified in the policy rule and performs the actions specified in the rule, if the conditions are met.
-   **[Create a cloud policy](../task/create-cloud-policy.md)**  
A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort workflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.
-   **[Create a cloud approval policy](../task/create-cloud-approval-policy.md)**  
A cloud approval policy specifies the users who must approve a specified cloud activity before the activity can proceed. Approvers can include the manager of the user making a request, a specified user or group, or users with a specified role. You can specify multiple approvers. Approvals occur in the order that you specify.
-   **[Create a cloud policy group](../task/create-cloud-policy-group.md)**  
A cloud policy group is a container for related policies. Consider grouping policies that are often used together or should be considered together. Grouping policies can help you to apply policies consistently across your organization.
-   **[Export or import a cloud policy](../task/export-import-policy.md)**  
To back up, move, or restore a policy, you can export and import the policy as an update set. The update set includes rules, conditions, actions, scripts, and script categories.

**Parent Topic:**[Cloud Admin Portal](cloud-admin-portal.md)

