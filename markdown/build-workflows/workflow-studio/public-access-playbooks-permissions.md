---
title: Public access playbooks permissions
description: Public access playbooks use their own authoring roles and follow restrictions that don't apply to other playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/public-access-playbooks-permissions.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Public access playbooks permissions

Public access playbooks use their own authoring roles and follow restrictions that don't apply to other playbooks.

A public access playbook runs for users who don't have a ServiceNow login. Because these users can't be granted standard roles, public access playbooks use their own authoring roles and follow a set of restrictions that don't apply to other playbooks.

For steps to set up and embed a public access playbook, see [Configure guest user access to playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-guest-user-access.md).

## Roles for authoring public access playbooks

-   **playbook.write.public\_access**

    Required to create and edit public access playbooks. Users without this role have read-only access. Delegated developers also require this role.

-   **playbook.content\_author.public\_access**

    Required to edit the public access field on an activity definition.

-   **playbook.automation\_runner**

    The restricted runner that automations use when executing in a public access playbook. Automations run with limited system access, not broad system privileges.


## Restrictions

Public access playbooks are subject to the following restrictions:

-   You can enable public access only when you create the playbook. You can't convert an existing playbook to public access.
-   A playbook must have a parent record because runtime permission checks depend on it. Standalone playbooks can't be made public.
-   Only activities with public access enabled can be included. Some activity definitions have public access enabled by default.
-   Only other public access playbooks can be nested inside a public access playbook.
-   Playbook type settings control which public features are allowed or blocked.
-   Guest users still need access to the parent record through access control rules. Public access doesn't bypass record-level security.
-   Runtime APIs and messaging channels require guest-safe access control rules and permission checks.
-   Automations can't be used directly. Wrap each automation in an activity definition before using it.
-   Any data that a guest user isn't authorized to view is hidden entirely, rather than displayed in a restricted form.

## Risks and considerations

A public access playbook is accessible to users you haven't authenticated. Review the following considerations before enabling public access:

-   **Data exposure through APIs and messaging**

    Guest users access the playbook through runtime APIs and messaging channels. The access control rules on those endpoints determine what data a guest user can retrieve.

-   **Flow data access**

    Automations in a public access playbook run under a restricted runner rather than with broad system access. Review what flow data the automations in your playbook can reach.

-   **Load from public users**

    Anyone who can reach the page where the playbook is embedded can start it. Plan for the volume of requests this may generate.

-   **Activity definition review**

    Enabling public access on an activity definition makes it available to all public access playbooks. Review each definition carefully before allowing public use.


**Parent Topic:**[Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-permissions.md)

