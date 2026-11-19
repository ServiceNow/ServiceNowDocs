---
title: Role-based access
description: Assign roles to control who can view, create, and edit playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/playbook-roles.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Role-based access

Assign roles to control who can view, create, and edit playbooks.

Playbook roles are hierarchical. A higher role contains the roles beneath it, so assigning playbook.admin grants every role below it in the hierarchy. For the full list of roles and what each one permits, see [Playbooks roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/process-automation-designer-roles.md).

**Note:** All users need the snc\_internal role to access internal resources, including playbooks. A user without it can encounter trigger validation errors when a playbook attempts to run. This is a platform requirement rather than a playbook role.

## Choosing a role

-   **pd\_author**

    Assign to users who author playbooks without restriction. Contains the write, designer access, and activity definition read roles. Grants access to use every activity definition when editing a playbook except for those activity definitions that specify Roles Required.

-   **playbook.write**

    Assign instead of pd\_author when content access filtering restricts what the user sees. Use it for cases where pd\_author is too broad a role. On its own it grants no read access to playbooks. Pair it with playbook.read or with a content access filtering rule to let users edit playbooks and use activity definitions. For more information, see [Content filtering for Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-filtering-playbooks.md).

-   **playbook.read**

    Assign to grant read-only access to all playbooks.

-   **playbook.designer\_access**

    Assign to let a user open Workflow Studio and view playbooks without granting edit rights.

-   **pd\_operator, pd\_cancel, and pd\_restarter**

    Assign to grant a single runtime capability without design-time access. The pd\_cancel role lets a user cancel a running playbook without holding playbook.admin or write access to the parent record. For example, use this to grant a manager an ability that agents don't have.


## Roles outside playbook administration

The playbook.designer\_access role contains two roles that playbook administrators don't manage. The sn\_workflow\_studio.workflow\_studio\_read role lets users to launch Workflow Studio. The sn\_diagram\_builder.db\_read role allows users to view playbooks in diagram view.

**Note:** Granting Playbooks roles doesn't grant access to the Workflow Studio design environment. Users who create activity definitions might also need Workflow Studio access. For more information, see [User access to Workflow Studio flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/user-access-flow-designer.md).

## Other ways to grant access

Roles are one of several mechanisms. To scope access to a single application, see [Delegated development access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/delegated-development-access.md). To restrict access to subsets of content, see [Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-access-filtering-playbooks.md). For an overview of every mechanism, see [Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-permissions.md).

**Parent Topic:**[Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-permissions.md)

