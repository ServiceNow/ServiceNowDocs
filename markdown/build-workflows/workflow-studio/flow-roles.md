---
title: Flow roles
description: Create flows and subflows that run with specific roles. Assigning roles enables you to create user-initiated flows that run with their own roles rather than the user's roles.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Flow roles

Create flows and subflows that run with specific roles. Assigning roles enables you to create user-initiated flows that run with their own roles rather than the user's roles.

## Role selection

A flow runs as either the system user or as the user who initiates the session. You can only assign roles to flows that run as the user who initiates the session. When the flow runs as the system user, it runs with the system role, and individual role selection isn't available. For more information, see [Create a flow in Workflow Studio](../task/create-flow.md).

You can assign multiple roles to a flow. Selecting new roles replaces the flow's original roles. If roles aren't selected, the flow runs with the roles of the user who initiates the session.

The roles you can select for a flow depend on the roles you have and the application scope of the flow. Assign any roles you that have access to in a particular scope, except high-security roles. You can't assign the following roles to a flow:

-   admin
-   security\_admin
-   application-specific admin roles, such as an application admin role for Human Resources.

## Modified and copied flows

Other users can modify and copy your flow. To modify a flow, a user must have the same roles as the flow. Users missing any of the roles assigned to the flow, sees the flow as read-only.

When you copy a flow, the assigned roles are removed. The copied flow runs with either the system role or the roles of the user who initiated the session.

## Missing roles

Sometimes a flow refers to a role that is not on the instance. The missing role may have been removed or may not exist on the instance. Either situation can occur when moving a flow between instances. When a role is unavailable, the **Run with role\(s\)** field displays the sys\_id of the role instead of its name. While the role is missing, you cannot save changes to the flow. To save flow changes, either remove the role from the flow or add it to the instance.

## Flow roles in execution details

You can see the "Run with" roles for a flow by viewing the flow execution details. Use the **Run As** field to determine which user ran the flow. Only flows that ran as the initiating user can have roles assigned. These flows have a **Run with role\(s\)** field that displays the roles assigned to the flow.

## Subflow roles

Flows and subflows each run with their own roles. Subflows don't inherit roles from a parent flow. When flow execution returns to a parent flow from a child flow, any special roles associated with the child flow are removed. The parent continues execution with its own roles.

## Access control lists

Assigning a role to a flow doesn't guarantee that the flow can access a record or table. While roles are an important part of access control lists \(ACLs\), they are just one possible condition. If a flow cannot access the records you expect it to, review the record ACL rules for the table and fields. The ACL rules might require additional criteria to grant access. For more information, see [access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).

## Flow roles override AI agent roles

A flow always runs using the roles it has been configured to run with in Workflow Studio. Flow roles override any roles inherited by an AI agent from a dynamic user or a specific AI user. If you want a flow to only run with the roles inherited from a user, remove flow roles. For information about adding roles to an AI agent, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

**Parent Topic:**[Building flows](flows.md)

