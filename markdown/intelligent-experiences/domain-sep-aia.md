---
title: Domain Separation AI agent
description: The Domain Visibility AI agent enables Domain Admins to manage user domain visibility using guided, conversational workflows in the Now Assist panel.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Platform AI agents, Now Assist AI assets, Enable AI experiences]
---

# Domain Separation AI agent

The Domain Visibility AI agent enables Domain Admins to manage user domain visibility using guided, conversational workflows in the Now Assist panel.

## Domain Separation AI agent overview

The agent performs validated operations on domain visibility data without requiring direct access to domain visibility tables.

Once enabled, the Domain Visibility agent exposes the following options to the admin:

-   List all domain visibility for a user
-   Add domain visibility for a user
-   Remove domain visibility from a user

**Note:** The agent interacts directly with the `sys_user_visibility` table. All domain visibility operations \(add, remove, list, query\) are executed through this table. Admins do not need to open or configure the table manually.

## Prerequisites and setup

Ensure the following requirements are met before using the AI agent:

-   The Domain Separation plugin is installed on your instance and active. For more information, refer to [Domain separation plugin](https://www.servicenow.com/docs/access?context=domain-sep-plugin&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   AI capabilities are enabled on the instance.
-   You are signed in with a Domain Admin role.

## Role masking

Required role: Domain Admin.

AI agents use [role masking](aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](../task/define-sec-controls-aia.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to evaluate for readiness. For example, you can add the itil role to the AI agent's list of approved roles so that it can access Incident records.

## Accessing the Issue Readiness AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Go to the **AI Agents** tab.
3.  Select **Domain Visibility**.

## Access the AI agent

1.  Open the Now Assist panel.
2.  Start a new interaction.
3.  Enter the prompt, "domain visibility help."

The agent displays the available domain visibility operations and guides you through the selected task.

## List all domain visibility for a user

Use this operation to view all domains a user can access.

1.  Select **List domain visibility** from the agent’s options.
2.  Provide the name of the user whose domain visibility you want to view.

The agent retrieves all domain visibility entries associated with the user.

## Add domain visibility for a user

Use this operation to grant a user visibility to a specific domain.

1.  Select **Add domain visibility** from the agent’s available options.
2.  Provide the requested inputs:
    -   **User name**
    -   **Domain name**
3.  The agent validates that the specified user and domain exist.
4.  Confirm the user name and domain name and that you want to add the visibility for the user.

The agent adds visibility for the specified domain to the specified user.

**Note:** You can verify this by checking the `sys_user_visibility` table.

## Remove domain visibility from a user

Use this operation to revoke a user’s visibility to a specific domain.

1.  Select **Remove domain visibility** from the agent’s available options.
2.  Provide the requested inputs:
    -   **User name**
    -   **Domain name**
3.  The agent validates that the specified user and domain exist and that the user currently has visibility to the specified domain.

    If no matching visibility exists, the agent reports that there is nothing to remove.

4.  If visibility does exist, confirm the user name and domain name and that you want to remove the visibility for the user.

The agent removes visibility for the specified domain from the specified user.

**Note:** You can verify this by checking the `sys_user_visibility` table.

**Parent Topic:**[Platform AI agents](platform-ai-agents.md)

