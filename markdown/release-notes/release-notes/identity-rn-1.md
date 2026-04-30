---
title: Identity release notes
description: The ServiceNow Identity application supports mechanisms that let you validate the identity of users. Identity was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Identity release notes

The ServiceNow® Identity application supports mechanisms that let you validate the identity of users. Identity was enhanced and updated in the Zurich release.

## Identity highlights for the Zurich release

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Configure AI Agents or AI users by selecting the `AI` option from the **Identity type** drop-down menu.
-   Use the `ai_user_admin` role for creating, editing, and role management of AI users. Using the role you can view, create, edit, assign roles to, and delete users with the identity type as `AI`.
-   Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions. To learn more, see [Role masking in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   Access Analyzer v.6 supports agentic workflows and AI agents in the Analyze Permissions feature.

    **Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).

-   Use Federated ID to uniquely identify roles across multiple instances. Federated ID provides a unique identifier for roles, making it easier to manage and track them across instances. To know more, see [Explore Federated ID](https://www.servicenow.com/docs/access?context=federated-id&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   View the Inbound API Integration Usage dashboard under the Machine Identity Console's Unique API calls page to access statistics for requestors and their API calls. To know more, see [Metrics](https://www.servicenow.com/docs/access?context=machine-identity-metrics&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and [View Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=view-inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

Zurich

-   Manage your non-human identities \(NHIs\) using the Machine Identity Console.
-   Support security data filter functionality in Applied or Undefined status and Controlled by Refs functionality during access control list \(ACL\) query.

    **Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


See [Identity](https://www.servicenow.com/docs/access?context=identity-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use the Machine Identity Console to see what data integration accounts are accessing and how they’re configured. This console helps you make smarter security decisions about setting up these accounts.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Access analyzer](https://www.servicenow.com/docs/access?context=access-analyzer&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Display the Security data filter that is in the **Applied** or **Undefined** status in the Access Analyzer results. Access Analyzer also supports the new criteria in ACLs that is controlled by reference.

    **Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


## Activation information

Identity is a ServiceNow AI Platform product that is active by default.

## Related ServiceNow applications and features

-   **[Secure your instance](https://www.servicenow.com/docs/access?context=platsec-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Platform Security is built into all levels of the ServiceNow AI Platform. Implement the security features that are appropriate for your organization. Manage failed log in and encrypted password protection, access control rules, and audit logs.


