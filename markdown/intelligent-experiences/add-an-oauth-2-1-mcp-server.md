---
title: Add an MCP Server with OAuth 2.1
description: Add an MCP Server with OAuth 2.1 in the AI Agent Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Adding an MCP Server in AI Agent Studio, Configuring Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP Server with OAuth 2.1

Add an MCP Server with OAuth 2.1 in the AI Agent Studio.

## Before you begin

Role required: sn\_mcp\_client.admin

## About this task

OAuth is the usual method to authenticate the MCP servers. If your MCP server supports it, choose OAuth 2.1 in the Authentication method.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  Navigate to **Manage MCP Servers** and select **New**.

3.  On the form, fill in the fields.

<table id="table_jnr_n3g_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your MCP Server.

</td></tr><tr><td>

Authentication Type

</td><td>

The authentication type with which you want to add your MCP Server.Select **OAuth 2.1**.

</td></tr><tr><td>

MCP Server URL

</td><td>

The web address of your MCP Server.

</td></tr></tbody>
</table>    ![Adding an MCP Server in AI Agent Studio with OAuth 2.1.](../image/mcp-server-oauth.png)

4.  Select **Next**.

    The form extends with the registration details.

5.  On the form, fill in the fields:

    The dynamic client registration auto-populates the data in the form fields.

    **Note:** If dynamic registration is supported by the MCP Server, you’ll be prompted to confirm the grant type and other inputs. If dynamic registration isn’t supported, you can continue with the Manual Registration method in Step 6.

<table id="table_zcx_vq3_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grant Type

</td><td>

The way you want to obtain an access token for accessing protected resources.One of the following two options is used here with auto-populated data.

-   **Authorization Code**: A system-generated code that is used for granting access to an application or resource.
-   **Client Credentials**: Access token provided by the administrator to access the application directly.


</td></tr><tr><td>

Token Authentication Method

</td><td>

Unique token granted to access resources.Select the value from the drop-down list.

</td></tr><tr><td>

Auth Scopes

</td><td>

Define the specific permissions for an application.**Note:** The Auth scopes must be comma-separated values.

</td></tr><tr><td>

Authentication Token for Client Registration

</td><td>

Authentication token used to verify client's identity and grant it permission to register with an authorization token.Provide the following values:

-   **Header**: Authorization header.
-   **Value**: Authentication password.


</td></tr><tr><td>

Authorization URL

</td><td>

Web address of your server to direct authorization.

</td></tr><tr><td>

Token URL

</td><td>

Web address containing the token.

</td></tr><tr><td>

Token Revocation URL

</td><td>

Web address to revoke the previously provided token.

</td></tr></tbody>
</table>    ![Dynamic client registration form with auto-populated data in the form fields.](../image/aouth-dynamic-client-registration.png)

    The MCP Server with dynamic client registration is added as a simple connection and credential alias.

6.  On the form, fill in the fields:

    **Note:**

    -   If your MCP Server doesn’t support Dynamic Client Registration, then you can register the OAuth client for AI agents in your MCP Server manually and update those client details in AI Agent Studio.
    -   The manual client registration doesn’t auto-populate the data in the form fields and must be manually provided.
<table id="table_yds_tsh_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grant Type

</td><td>

The way you want to obtain an access token for accessing protected resources.You can select one of the two options:

-   **Authorization Code**: A system-generated code that is used for grating access to an application or resource.
-   **Client Credentials**: Access token provided by the administrator to access the application directly.


</td></tr><tr><td>

Token Authentication Method

</td><td>

Unique token granted to access resources.Select the value from the drop-down list.

</td></tr><tr><td>

Client ID

</td><td>

Unique ID for authentication and authorization purposes.

</td></tr><tr><td>

Client Secret

</td><td>

Unique credentials used for authentication.

</td></tr><tr><td>

Auth Scopes

</td><td>

Define the specific permissions for an application.**Note:** The Auth scopes must be comma-separated values.

</td></tr><tr><td>

Authentication Token for Client Registration

</td><td>

Authentication token used to verify client's identity and grant it permission to register with an authorization token.Provide the following values:

-   **Header**: Authorization header.
-   **Value**: Authentication password.


</td></tr><tr><td>

Authorization URL

</td><td>

Web address of your server to direct authorization.

</td></tr><tr><td>

Token URL

</td><td>

Web address containing the token.

</td></tr><tr><td>

Token Revocation URL

</td><td>

Web address to revoke the previously provided token.

</td></tr></tbody>
</table>    ![Manual client registration for an OAuth MCP Server.](../image/mcp-server-manual-registration.png)

7.  Select **Add**.

    Selecting Add takes you to the MCP Server record where you must authenticate it for adding an MCP tool to an AI agent.

8.  Select **Authenticate**.

    Selecting **Authenticate** takes you to the third-party authorization page where you must select a workspace and select **Authorize**.

    **Note:** When the OAuth access or refresh tokens aren’t available, you must authenticate the OAuth configuration on the MCP Server record to add it as a tool to an AI agent.


