---
title: Identity release notes
description: The ServiceNow Identity application supports mechanisms that let you validate the identity of users. Identity was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Identity release notes

The ServiceNow® Identity application supports mechanisms that let you validate the identity of users. Identity was enhanced and updated in the Australia release.

## Identity highlights for the Australia release

-   Use the granular roles to complete administrative configuration tasks for Identity without requiring the full admin role.
-   Configure AI Agents or AI users by selecting the `AI` option from the Identity type drop-down menu.
-   Use the ai\_user\_admin role for creating, editing, and role management of AI users. Using the role you can view, create, edit, assign roles to, and delete users with the identity type as `AI`.
-   Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.
-   Use the Identity sub-type field to categorize the identity type while creating a user.

See [Identity](https://www.servicenow.com/docs/access?context=identity-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    The granular admin role enables developers and administrators to complete administrative configuration tasks for Identity without requiring the full admin role.


## Changed in this release

-   **[Role masking in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.

-   **[User management enhancements](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    User management enhancements:

    -   Configure AI agents or AI users by selecting the `AI` option from the Identity type drop-down menu.
    -   Use the ai\_user\_admin role for creating, editing, and role management of AI users. Use this role to view, create, edit, assign roles to, and delete users with the identity type as `AI`.
    -   Use the Identity sub-type field to categorize the identity type while creating a user.
    -   Use the new date and time formats based on the user's preference while creating users.
-   **[Federated ID](https://www.servicenow.com/docs/access?context=federated-id&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Use Federated ID to uniquely identify roles across multiple instances. Federated ID provides a unique identifier for roles, making it easier to manage and track them across instances.

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    View the Inbound API Integration Usage dashboard under the Machine Identity Console's Unique API calls page to access statistics for requesters and their API calls.


-   **[Scripting Governance Tool](https://www.servicenow.com/docs/access?context=scripting-governance&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Manage user permissions for scripting on the ServiceNow AI Platform from the enhanced scripting governance tool.


## Activation information

Identity is a ServiceNow AI Platform product that is active by default.

## Accessibility information

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Related ServiceNow applications and features

-   **[Secure your instance](https://www.servicenow.com/docs/access?context=platsec-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Platform Security is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed log in and encrypted password protection, access control rules, and audit logs.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

