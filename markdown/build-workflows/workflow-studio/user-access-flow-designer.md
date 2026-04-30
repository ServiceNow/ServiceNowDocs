---
title: User access to Workflow Studio flows
description: Administrators can grant users access to Workflow Studio flows by assigning delegated development permissions or directly assigning a user role. Administrators can also specify which features and content a user can access based on user roles. Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-12-11"
reading_time_minutes: 5
breadcrumb: [Flows, Configure, Workflow Studio, Build workflows]
---

# User access to Workflow Studio flows

Administrators can grant users access to Workflow Studio flows by assigning delegated development permissions or directly assigning a user role. Administrators can also specify which features and content a user can access based on user roles. Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions.

## Access by user role

Administrators can grant access to Workflow Studio flows by directly assigning users the flow\_designer user role, which includes the role to view flow execution details.

**Warning:** Directly granting a user the flow\_designer role is equivalent to giving the user the admin role, because Workflow Studio can run flows as the System user, which has access to all tables and all database operations.

Administrators can also grant users one or more Workflow Studio roles to enable them to create flows and subflows, view flow execution details, and create actions.

<table id="table_utq_v2r_nnb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

flow\_designer

</td><td>

Enables you to launch the Workflow Studio flow design environment to create and edit flows and subflows.

</td><td>

flow\_operator, trigger\_designer

</td></tr><tr><td>

flow\_designer\_scripting

</td><td>

Enables someone with the flow\_designer or action\_designer role to set and modify input values by writing inline scripts. For information, see [Inline scripts](inline-scripts.md).

</td><td>

none

</td></tr><tr><td>

flow\_operator

</td><td>

Enables you to view flow execution details, dashboards, and logs. Administrators can grant this role to users that want to be able to view flow results but not create, change, or test them.

</td><td>

none

</td></tr><tr><td>

flow\_report\_viewer

</td><td>

Enables you to view reports for Workflow Studio flow tables. For a list of relevant flow reporting tables, see [Flow execution details retention](flow-reporting.md).

</td><td>

none

</td></tr><tr><td>

trigger\_designer

</td><td>

Enables you to launch Workflow Studio and create, edit, and delete a saved trigger.

</td><td>

none

</td></tr><tr><td>

action\_designer

</td><td>

Enables you to launch the Workflow Studio action design environment to create and edit actions.**Important:** This role provides access to all actions regardless of their application scope.

</td><td>

none

</td></tr><tr><td>

action\_category\_creator

</td><td>

Enables someone with the action\_designer role to create action categories for actions and subflows.

</td><td>

none

</td></tr><tr><td>

fd\_read

</td><td>

Enables you to launch the Workflow Studio flow and action design environments to view the configuration and execution details of flows, subflows, and actions.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

fd\_read\_flows, fd\_read\_actions, fd\_read\_operations

</td></tr><tr><td>

fd\_read\_flows

</td><td>

Enables you to launch the Workflow Studio flow design environment to view the configuration and execution details of flows and subflows.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

fd\_read\_operations

</td></tr><tr><td>

fd\_read\_actions

</td><td>

Enables you to launch the Workflow Studio action design environment to view the configuration of actions.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

none

</td></tr><tr><td>

fd\_read\_operations

</td><td>

Enables you to view basic flow and action execution details. When reporting is enabled, you can only see basic execution details such as the runtime state and duration. If the reporting level generates additional details, you can't see them. Administrators can grant this role to users that only need to view basic execution results but not create, change, or test flows and actions.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

none

</td></tr><tr><td>

fd\_read\_operations\_all

</td><td>

Enables you to view all generated flow and action execution details. When reporting is enabled, you can view all available execution details. You can only see as much detail as defined by the reporting level system property. Administrators can grant this role to users that need to view all flow results but not create, change, or test flows and actions.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

fd\_read\_operations

</td></tr></tbody>
</table>**Note:** Some applications provide UI actions to view related flow or flow contexts. You need an application-specific user role to view such UI actions. For example, users require the **itil** or equivalent user role to view the **Flow Context** UI action available from Requested Item records.

## API access

Application developers can access Workflow Studio functionality through APIs for flows, subflows, and actions. Flow authors can enable individual flows, subflows, and actions to be client callable during design. For more information, see [API access to Workflow Studio flows](api-access-flow-designer.md).

## Delegated development access

Administrators can grant users access to Workflow Studio flows by creating an application and assigning users as developers with the [delegated development](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=zurich&pubname=zurich-application-development&ft:locale=en-US) permission. Delegated development allows administrators to control whether flow designers can access features normally restricted to admin users such as assigning user roles, creating access controls, or creating scripts. For more information, see [Developer permissions](https://www.servicenow.com/docs/access?context=developer-permissions&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Role-based content filtering

Specify the user roles necessary to access Workflow Studio flow content. For example, flows, flow triggers, actions, and subflows. Manage content filtering by creating content definitions and content filtering rules. For more information, see [Content filtering for Workflow Studio flows](content-filtering-flow-designer.md).

**Note:** Your users must have the flow\_designer role to create and edit flows. You can specify the additional roles that a user must have to access particular features or content.

## Role-based feature access

Specify additional user roles necessary to access the UI elements of Workflow Studio flows. For example, specify a role to access the buttons to save, test, or activate a flow or to access the option to copy a code snippet. Manage feature access directly through the Feature Access List. For more information, see [Manage access to Workflow Studio flow features](../task/manage-access-features.md).

**Note:** Your users must have the flow\_designer role to create and edit flows. You can specify the additional roles that a user must have to access particular features or content.

-   **[Manage access to Workflow Studio flow features](../task/manage-access-features.md)**  
 Restrict access to individual Workflow Studio flow features by user role. Specify what additional roles a user must have to access an individual feature such as copy a flow.
-   **[Content filtering for Workflow Studio flows](content-filtering-flow-designer.md)**  
Specify which content a user can access based on the user's role.

**Parent Topic:**[Configuring flows](configuring-flow-designer.md)

