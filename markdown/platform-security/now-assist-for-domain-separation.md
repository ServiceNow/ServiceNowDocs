---
title: Now Assist for Domain Separation
description: The Domain Visibility AI agent enables Domain Admins to manage user domain visibility using guided, conversational workflows in the Now Assist panel. The agent performs validated operations on domain visibility data without requiring direct access to domain visibility tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Domain separation for service providers, Access Management]
---

# Now Assist for Domain Separation

The Domain Visibility AI agent enables Domain Admins to manage user domain visibility using guided, conversational workflows in the Now Assist panel. The agent performs validated operations on domain visibility data without requiring direct access to domain visibility tables.

Once enabled, the Domain Visibility agent exposes the following options to the admin:

-   List all domain visibility for a user
-   Add domain visibility for a user
-   Remove domain visibility from a user
-   Query who has access to which domains

**Note:** The agent interacts directly with the `sys_user_visibility` table. All domain visibility operations \(add, remove, list, query\) are executed through this table. Admins do not need to open or configure the table manually.

## Before you begin

Ensure the following requirements are met before using the AI agent:

-   The Domain Separation plugin is installed on your instance and active. For more information, refer to [Domain separation plugin](../concept/domain-sep-plugin.md).
-   The Gen AI Controller bundle is installed on your instance and active. For more information, refer to [Installing the Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   AI capabilities are enabled on the instance.
-   You are signed in with a Domain Admin role.

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

## Query who has access to which domains

Use this capability to understand domain access relationships without directly querying tables.

To do so, submit a query‑style prompt through the agent. For example, `"Who has access to the ACME domain?"`.

The agent returns a summarized, user‑friendly view of all domain access. Results are provided directly in the Now Assist panel, without requiring manual table access.

