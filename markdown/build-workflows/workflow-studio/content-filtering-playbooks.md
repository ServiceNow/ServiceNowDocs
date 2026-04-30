---
title: Content filtering for playbooks
description: Specify which content a user can access based on the user's role.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [User access to playbooks in Workflow Studio, Administering playbooks, Configuring playbooks, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Content filtering for playbooks

Specify which content a user can access based on the user's role.

Display only content that is relevant for a particular user, hiding content that is unnecessary or sensitive. Specify the Workflow Studio playbook content that you want to control access to and the role that a user must have to access it. For example, if a user with the guided\_decision\_builder role is creating a playbook, show only a relevant set of activities.

To implement content filtering, you need:

-   Content definitions to specify types of content.
-   Content filtering rules and roles to determine who can access the content.

There is one content definition for playbooks by default, the **Playbooks - All Activity Definitions** content definition. The **Playbooks - All Activity Definitions** content definition has two content filtering rules by default:

-   **\(Default\) Playbook - Users with delegated\_developer role can access all activity definitions**
-   **\(Default\) Playbook - Users with playbook.activity\_def\_read role can access all activity definitions**

This means that users with the roles delegated\_developer or playbook.activity\_def\_read role can access all activity definitions. Get started with content filtering by using default definitions and rules, or create your own.

## Content definitions

Content definitions specify a type of Workflow Studio resource. Resources are key elements of Workflow Studio components, such as activity definitions for playbooks. Create content definitions to include an entire resource, or use a condition builder to refine your definitions. For example, the content definition for playbook activity definitions includes all activity definitions, but you could create a content definition that includes only the activity definitions that contain Guided Decision in the **Name** or **Package**.

You can further refine content definitions through tagging. Add resource tags to items in a resource list, then design your content definition to only include resources with that tag.

## Content filtering rules

Content filtering rules specify the role that a user must have to access the content in a particular definition. Each rule associates a single user role with a single content definition. When a user accesses Workflow Studio playbooks, content filtering rules determine what activities the user may access based on the user's role.

## Role-based activity definition access

Manage activity definition access by specifying the **Required Roles** to access an activity definition. To learn more about roles, see [Playbooks roles](../reference/process-automation-designer-roles.md). To learn more about activity definitions, see [Activity definitions](activity-definitions.md).

![Required roles field in an activity definition](../images/required-roles-activity-def.png)

**Note:** Both playbook.admin and pd\_content\_author roles can edit activity definitions, but only the playbook.admin role can edit the **Required Roles** field.

## Restricted playbooks

Users cannot view a playbook that contains activities that they do not have access to. When a playbook contains restricted activities, the entire playbook is restricted.

<table><thead><tr><th>

Resource filtered

</th><th>

User has role

</th><th>

User does not have role

</th></tr></thead><tbody><tr><td>

Activity Definition

</td><td>

-   The activity definition is visible to select when building a playbook.
-   The activity definition can be copied.
-   The activity definition can be modified.

</td><td>

-   The activity definition is hidden and cannot be selected when building a playbook.
-   Playbooks with the activity definition are not visible.

</td></tr></tbody>
</table>## Design considerations

-   **Content definition roles for activity definitions**

    Give users access to the subset of activity definitions in a content definition by assigning the playbook.write role, not the pd\_author role.


**Parent Topic:**[User access to playbooks in Workflow Studio](user-access-playbooks.md)

