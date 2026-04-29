---
title: Playbooks roles
description: Grant users one or more Playbooks roles to enable them to create triggers, playbooks, and activity definitions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Playbooks roles

Grant users one or more Playbooks roles to enable them to create triggers, playbooks, and activity definitions.

## Roles

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and contact your account representative.

System administrators can grant users access to Playbooks by assigning [delegated development permissions](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US) or directly assigning [Roles](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US). Additionally, playbook authors can create additional filters for runtime user access as they build a playbook in Workflow Studio. The following user roles are available for Playbooks:

<table id="table_h1y_drx_blb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

playbook.admin

</td><td>

Enables users to:-   Create, update, and delete trigger definitions.
-   Launch Workflow Studio to create, activate, edit, and delete playbooks.
-   Create, edit, and delete activity definitions.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.
-   Add translations for a playbook.

</td></tr><tr><td>

pd\_author

</td><td>

Enables users to:-   Launch Workflow Studio to create, activate, edit, and delete playbooks.
-   View all activity definitions.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td></tr><tr><td>

pd\_content\_author

</td><td>

Enables users to:-   Create, edit, and delete activity definitions.
-   Create, edit, and delete trigger definitions.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td></tr><tr><td>

pd\_trigger\_author

</td><td>

Enables users to create, update, and delete trigger definitions.

</td></tr><tr><td>

pd\_operator

</td><td>

Enables users to view process executions, activity executions, and execution logs only.

</td></tr><tr><td>

pd\_shared.user

</td><td>

Enables users to view the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td></tr><tr><td>

pd\_shared.admin

</td><td>

Enables users to edit the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

</td></tr><tr><td>

pd\_cancel

</td><td>

Enables users to cancel running playbooks without the playbook.admin role or write access to the parent record. For example if you want to grant an agent manager the ability to cancel playbooks, but not an agent.

</td></tr><tr><td>

pd\_restarter

</td><td>

Enables users to restart active playbooks.

</td></tr><tr><td>

playbook.write

</td><td>

Enables users who have content filtering restrictions to:-   Launch Workflow Studio to create, activate, edit, and delete playbooks.
-   View the Experience activity types \(sys\_pd\_activity\) and Experience activity properties \(sys\_pd\_activity\_type\_prop\) tables that are shared by Playbooks and Playbook Experience.

To learn more about content access filtering, see [Content filtering for Playbook](../concept/content-filtering-playbooks.md)

</td></tr><tr><td>

playbook.designer\_access

</td><td>

Enables users who have content filtering restrictions to launch Workflow Studio to view playbooks. To learn more about content access filtering, see [Content filtering for Playbook](../concept/content-filtering-playbooks.md).

</td></tr><tr><td>

playbook.activity\_def\_read

</td><td>

Enables users to view all activity definitions as long as there aren't [Required Roles](../concept/content-filtering-playbooks.md#activity_def_req_roles).

</td></tr></tbody>
</table>**Note:** Granting users Playbooks roles does not automatically allow them to access the Workflow Studio design environment. Granting users access to Workflow Studio may be helpful when creating activity definitions. For more information on Workflow Studio roles, see [user access to Flow Designer](../../flow-designer/concept/user-access-flow-designer.md).

