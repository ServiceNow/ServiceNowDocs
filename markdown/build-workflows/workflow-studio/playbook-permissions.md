---
title: Managing playbook permissions
description: Understand which mechanisms control who can build playbooks and who can interact with them while they run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/playbook-permissions.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [roles, access, runtime permissions, delegated]
breadcrumb: [Configure, Playbooks, Workflow Studio, Build workflows]
---

# Managing playbook permissions

Understand which mechanisms control who can build playbooks and who can interact with them while they run.

Playbooks control access through four mechanisms, each layered on top of the platform access control rules that apply to every table. Each mechanism serves a different purpose, and many configurations use more than one.

Two requirements apply regardless of which mechanism you use: all users need the snc\_internal role to access internal resources, and completing an activity requires write access to that activity's Experience Status Record.

## The four mechanisms

-   **Roles**

    Grant broad access. The pd\_author role grants full create, update, and delete access to all playbooks. Grants access to use every activity definition when editing a playbook except for those activity definitions that specify Roles Required. Use playbook.write for cases where pd\_author is too broad a role. On its own it grants no read access to playbooks. Pair it with playbook.read or with a content access filtering rule to let users edit playbooks and use activity definitions. Roles are hierarchical, so a higher-level role includes all roles beneath it. For more information, see [Role-based access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-roles.md).

-   **Delegated development**

    Scope playbook access to edit playbook content within a single application, including Playbooks and Activity Definitions. Users can still use activity definitions from other scopes within their playbook. For more information, see [Delegated development access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/delegated-development-access.md).

-   **Content access filtering**

    Restricts access to specific content at design time. Create a content definition that describes the content, then create a filtering rule that specifies which roles can access it. You can filter by activity definition, by playbook type, or by resource tag. Use it when a role grants more access than a user should have. For example, the pd\_author role allows users to edit any playbook and use any activity definition. You can grant a user playbook.write, which only lets them edit playbooks and use activity definitions that have been granted to them through content access filtering. For more information, see [Content filtering for Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-filtering-playbooks.md).

-   **Runtime permissions**

    Controls which users can view and interact with a playbook that is already running. Playbook authors configure these settings during the build process, at the playbook and stage level. For more information, see [Runtime permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/runtime-permissions-playbooks.md).


Public access playbooks are a playbook setting, not a separate mechanism. Enabling public access adds restrictions and removes none. For more information, see [Public access playbooks permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/public-access-playbooks-permissions.md).

## Design time and runtime

Roles, delegated development, and content access filtering control who can build and edit playbooks. Runtime permissions control who can act on a playbook that is already running.

Users need both types of access. Design-time mechanisms determine what someone can build. Runtime permissions determine what someone can do with a running playbook. To view a running playbook, a user must have read access on its parent record in addition to any custom permissions defined by the playbook author.

Administrators configure design-time mechanisms in the platform UI, and those apply across the instance. Playbook authors configure runtime permissions inside Workflow Studio while building, and those apply to one playbook.

## Choosing a mechanism

|Goal|Mechanism|
|----|---------|
|Let someone author playbooks without restriction|The pd\_author role|
|Let someone author playbooks in one application only|Delegated development|
|Give read-only access to all playbooks|The playbook.read role|
|Show someone a subset of activity definitions|Content access filtering with the playbook.write role|
|Restrict access to edit a subset of playbooks|Content access filtering with the playbook.write role|
|Restrict one activity definition to a named role|Required roles on the activity definition|
|Let an operator cancel any playbook|The pd\_cancel role|
|Restrict who can restart a playbook or add optional activities|Runtime permissions on the playbook|
|Run a playbook for users who have no login|Public access playbooks|
|Let a specific user or group complete an activity|Assignment on the activity's Experience Status Record|

## How the mechanisms interact

Using multiple mechanisms together is common. The following rules explain what happens when mechanisms overlap.

-   **Roles accumulate**

    Assigning a role grants all permissions that role includes. Assigning playbook.admin grants every playbook role beneath it.

-   **Required roles override content access filtering**

    A user without the required role can't use an activity definition even when a content filtering rule grants access to it.

-   **Access control rules are a separate layer**

    Read access control rules on playbook tables can call into content access filtering logic. This means a user can be blocked by an access control rule even when a content filtering rule grants access. For more information, see [Access control rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/access-control-rules-playbooks.md).

-   **Runtime permissions only narrow access**

    The parent record defaults are required and can't be removed. Anything an author adds is a further condition. A playbook with runtime permissions configured is more restrictive than one without, never less.

-   **Default permissions combine with AND; added permissions combine with OR**

    Read access on a playbook where the author added two roles resolves to read access on the parent record AND membership of the first role OR the second.

-   **Runtime overrides cascade downward**

    A stage overrides the playbook. The most specific configuration takes precedence.

-   **Read-only has several causes, only some related to permissions**

    A user who can't access every activity definition in a playbook sees a read-only view of that playbook, not a partial view. The same applies to a user without write access to the process definition. However, when a user is viewing a running playbook, an activity's form appears as read-only if there is no declarative action that requires form fields. This is a configuration issue rather than a permissions issue. Before concluding that a user lacks access, check declarative actions on the activity, the user's access to the activity definitions, and their write access to the process definition.

-   **Completing an activity is governed separately**

    Reading an activity and completing it are different operations with different sources. Read access comes from runtime permissions and the parent record. Completing or skipping depends on write access to the activity's Experience Status Record.

-   **Public access adds restrictions to every mechanism**

    A role or filtering rule that grants access in an ordinary playbook may grant less in a public access playbook. Guest users still need access to the parent record, only activities with public access enabled can be used, and only public access playbooks can be nested. For more information, see [Public access playbooks permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/public-access-playbooks-permissions.md).


-   **[Role-based access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-roles.md)**  
Assign roles to control who can view, create, and edit playbooks.
-   **[Delegated development access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/delegated-development-access.md)**  
Delegated development scopes playbook access to edit Playbook content within a single application, including Playbooks and Activity Definitions. Users can still use activity definitions from other scopes within their playbooks.
-   **[Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/content-access-filtering-playbooks.md)**  
Restrict access to subsets of playbook content by pairing a content definition with a filtering rule.
-   **[Access control rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/access-control-rules-playbooks.md)**  
Access control rules operate at the platform level, independently of playbook permissions. A user can satisfy every playbook permission and still be blocked.
-   **[Runtime permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/runtime-permissions-playbooks.md)**  
Runtime permissions restrict who can read, restart, cancel, and add optional activities to a running playbook.
-   **[Public access playbooks permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/public-access-playbooks-permissions.md)**  
Public access playbooks use their own authoring roles and follow restrictions that don't apply to other playbooks.

**Parent Topic:**[Configuring Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/setting-up-process-automation-designer.md)

