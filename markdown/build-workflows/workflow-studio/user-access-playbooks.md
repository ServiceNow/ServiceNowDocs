---
title: User access to Playbooks in Workflow Studio
description: Administrators can grant users access to Playbook by assigning delegated development permissions or directly assigning a user role. Administrators can also specify which features and content a user can access based on user roles.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administering Playbooks, Configure, Playbooks, Workflow Studio, Build workflows]
---

# User access to Playbooks in Workflow Studio

Administrators can grant users access to Playbook by assigning delegated development permissions or directly assigning a user role. Administrators can also specify which features and content a user can access based on user roles.

## Access by user role

Administrators can grant access to Playbook in Workflow Studio by directly assigning users the pd\_author user role, which includes the role to view activity definitions.

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

playbook.admin

</td><td>

Enables users to:-   Create, update, and delete trigger definitions.
-   Launch Workflow Studio to create, activate, edit, and delete playbooks.
-   Create, edit, and delete activity definitions.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td><td>

-   pd\_author
-   pd\_content\_author
-   pd\_trigger\_author
-   pd\_operator
-   pd\_cancel

</td></tr><tr><td>

pd\_author

</td><td>

Enables users to:-   Launch Workflow Studio to create, activate, edit, and delete playbooks.
-   View all activity definitions.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td><td>

-   pd\_shared.user
-   playbook.write
-   playbook.activity\_def\_read

</td></tr><tr><td>

pd\_content\_author

</td><td>

Enables users to:-   Create, edit, and delete activity definitions.
-   Create, edit, and delete trigger definitions.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td><td>

-   pd\_trigger\_author
-   pd\_shared.user
-   playbook.activity\_def\_read

</td></tr><tr><td>

pd\_trigger\_author

</td><td>

Enables users to create, update, and delete trigger definitions.

</td><td>

none

</td></tr><tr><td>

pd\_operator

</td><td>

Enables users to view process executions, activity executions, and execution logs only.

</td><td>

none

</td></tr><tr><td>

pd\_shared.user

</td><td>

Enables users to view the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td><td>

none

</td></tr><tr><td>

pd\_shared.admin

</td><td>

Enables users to edit the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td><td>

pd\_shared.user

</td></tr><tr><td>

pd\_cancel

</td><td>

Enables users to cancel running playbooks without the playbook.admin role or write access to the parent record. For example if you want to grant an agent manager the ability to cancel playbooks, but not an agent.

</td><td>

none

</td></tr><tr><td>

pd\_restarter

</td><td>

Enables users to restart active playbooks.

</td><td>

none

</td></tr><tr><td>

playbook.write

</td><td>

Enables users who have content filtering restrictions to:-   Launch Workflow Studio to create, activate, edit, and delete playbooks.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

To learn more about content access filtering, see [Content filtering for Playbook](content-filtering-playbooks.md).

</td><td>

pd\_shared.user

</td></tr><tr><td>

playbook.designer\_access

</td><td>

Enables users who have content filtering restrictions to launch Workflow Studio to view playbooks. To learn more about content access filtering, see [Content filtering for Playbook](content-filtering-playbooks.md).

</td><td>

pd\_shared.user

</td></tr><tr><td>

playbook.activity\_def\_read

</td><td>

Enables users to view all activity definitions as long as there aren't [Required Roles](content-filtering-playbooks.md#activity_def_req_roles).

</td><td>

none

</td></tr></tbody>
</table>A visual representation of where roles are contained:

-   playbook.admin
    -   pd\_content\_author
        -   playbook.activity\_def\_read
        -   pd\_shared.user
        -   pd\_trigger\_author
    -   pd\_operator
    -   pd\_cancel
    -   pd\_restarter
    -   pd\_author
        -   playbook.write
            -   playbook.designer\_access
                -   pd\_shared.user
                -   sn\_workflow\_studio.workflow\_studio\_read

                    **Note:** This role allows users to launch Workflow Studio, and is not managed by playbook administrators.

                -   sn\_diagram\_builder.db\_read

                    **Note:** This role allows users to view playbooks in the diagram view in Workflow Studio, and is not managed by playbook administrators.

        -   playbook.activity\_def\_read
    -   pd\_shared.admin
        -   pd\_shared.user
-   delegated\_developer

## Delegated development access

Administrators can grant users access to Workflow Studio playbooks by creating an application and assigning users as developers with the playbook [delegated development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md) permission. Delegated development allows administrators to control whether playbook authors can access features normally restricted to admin users. For more information, see [Developer permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/developer-permissions.md).

## Role-based content filtering

Specify the user roles necessary to access Workflow Studio playbook content. For example, activity definitions and process definitions. Manage content filtering by creating content definitions and content filtering rules. For more information, see [Content filtering for Playbook](content-filtering-playbooks.md).

## Role-based activity definition access

Manage activity definition access by specifying the **Required Roles** to access an activity definition. Users who can view the playbook but who do not have the required role to access activities with this activity definition will have a read-only view of the playbook.

![Read-only view of activities in Workflow Studio for restricted activity definitions](../images/activity-definition-read-only.gif)

To learn more about activity definitions, see [Create an activity definition](../task/create-activity-definition.md) and [Activity definitions](activity-definitions.md).

**Note:** Both playbook.admin and pd\_content\_author roles can edit activity definitions, but only the playbook.admin role can edit the **Required Roles** field.

-   **[Content filtering for Playbook](content-filtering-playbooks.md)**  
Specify which content a user can access based on the user's role.
-   **[Configure content filtering definitions for Playbook](../task/configure-content-filtering-definitions-playbooks.md)**  
Specify which content a user can access by creating content definitions.
-   **[Configure content filtering rules for Playbook](../task/configure-content-filtering-rules-playbooks.md)**  
Use content filtering rules to specify the role a user must have to access content.

**Parent Topic:**[Administering Playbooks](administering-process-automation-designer.md)

