---
title: Add an MCP server with OAuth 2.1
description: Add an MCP server with OAuth 2.1 in the AI Agent Studio.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 3
breadcrumb: [Add an MCP server in AI Agent Studio, Configure Model Context Protocol Client, Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Add an MCP server with OAuth 2.1

Add an MCP server with OAuth 2.1 in the AI Agent Studio.

## Before you begin

Role required: sn\_mcp\_client.admin

## About this task

OAuth is the standard method to authenticate MCP servers. If your MCP server supports it, choose OAuth 2.1 as the authentication method.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  Navigate to **Manage MCP Servers** and select **New**.

3.  On the Add MCP server form, enter a name and the web address for your MCP server.

4.  In the **Authentication Type** field, select **OAuth 2.1**.

    ![Screenshot that shows the Add MCP Server form and its fields.](../image/mcp-server-oauth.png)

5.  Select **Next**.

    The form extends with the registration details.

6.  On the form, fill in the fields.

    The Dynamic Client Registration form auto-populates the field data.

    **Note:** If dynamic registration is supported by the MCP server, you're prompted to confirm the grant type and other inputs. If dynamic registration isn’t supported, you can continue to the Manual Registration method.

<table id="table_zcx_vq3_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grant Type

</td><td>

How you want to obtain an access token when accessing protected resources.The following options are available:

-   **Authorization Code**: A system-generated code used for granting access to an application or resource.
-   **Client Credentials**: An access token provided by the administrator to access the application directly.


</td></tr><tr><td>

Token Authentication Method

</td><td>

Method using which the client credentials are sent when requesting tokens from the Authorization server.

</td></tr><tr><td>

Auth Scopes

</td><td>

Specific permissions for an application.**Note:** The Auth scopes must be comma-separated values.

</td></tr><tr><td>

Authentication Token for Client Registration

</td><td>

Authentication token used to verify the identity of the client and grant it permission to register with an authorization token.Provide the following values:

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

Web address to revoke the previously provided token in the Authentication Token for Client Registration field.

</td></tr></tbody>
</table>    ![Dynamic client registration form with auto-populated data in the form fields.](../image/aouth-dynamic-client-registration.png)

    The MCP server with dynamic client registration is added as a simple connection and credential alias.

7.  On the form, fill in the fields.

    **Note:**

    -   If your MCP server doesn’t support dynamic client registration, then you can register the OAuth client for AI agents in your MCP server manually and update those client details in AI Agent Studio.
    -   The manual registration doesn’t auto-populate the field data and must be manually provided.
<table id="table_yds_tsh_xfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grant Type

</td><td>

How you want to obtain an access token when accessing protected resources.The following options are available:

-   **Authorization Code**: A system-generated code used for granting access to an application or resource.
-   **Client Credentials**: An access token provided by the administrator to access the application directly.


</td></tr><tr><td>

Token Authentication Method

</td><td>

Method using which the client credentials are sent when requesting tokens from the Authorization server.

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

Specific permissions for an application.**Note:** The Auth scopes must be comma-separated values.

</td></tr><tr><td>

Authentication Token for Client Registration

</td><td>

Authentication token used to verify the identity of the client and grant it permission to register with an authorization token.Provide the following values:

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

8.  Select **Add**.

    You're redirected to the MCP Server record to authenticate the MCP server for adding an MCP tool to an AI agent.

9.  Select **Authenticate**.

10. In the third-party authorization page, select **Authorize**.

    **Note:** When OAuth access or refresh tokens aren’t available, you must authenticate the OAuth configuration on the MCP server record to add it as an AI agent tool.


