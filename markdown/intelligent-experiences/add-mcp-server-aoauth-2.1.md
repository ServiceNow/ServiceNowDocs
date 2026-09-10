---
title: Add an MCP server with OAuth 2.1
description: Add an MCP server with OAuth 2.1 in the AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-mcp-server-aoauth-2.1.html
release: australia
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 2
breadcrumb: [Adding an MCP Server Console in AI Agent Studio, Configuring Model Context Protocol Client, MCP Client, AI Agent Studio, Enable AI experiences]
---

# Add an MCP server with OAuth 2.1

Add an MCP server with OAuth 2.1 in the AI Agent Studio.

## Before you begin

Role required: sn\_mcp\_client.admin

## About this task

OAuth is the standard method to authenticate MCP servers. If your MCP server supports it, choose OAuth 2.1 as the authentication method.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings** &gt; **Manage Model Contextual Protocol \(MSCP\) Servers**.

2.  Select **View** against **MCP Servers**.

3.  On the Model Context Protocol Server page, select **New**.

4.  On the Add MCP Server Console form, enter a name and the web address for your MCP server.

5.  In the **Authentication Type** field, select **OAUTH 2.1**.

    \[Omitted image "add-mcp-server-new.png"\] Alt text: Screenshot that shows the Add MCP Server form and its fields.

6.  Select **Next**.

    The form extends with the registration details.

7.  On the form, fill in the fields.

    **Note:**

    -   If your MCP server doesn’t support dynamic client registration, register the OAuth client for AI agents manually. Update the client details in AI Agent Studio.
    -   The manual registration doesn’t auto-populate the field data and must be manually provided.
    \[Omitted image "add-mcp-server-oauth-manual.png"\] Alt text: Manual client registration for an OAuth MCP Server.

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

Method using which the client credentials are sent when requesting tokens from the Authorization server.You can one of the two options:

-   **Client Secret Basic**
-   **Client Secret Post**


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
</table>8.  Select **Add**.

    You're redirected to the Model Context Protocol Server Console record to authenticate the MCP server for adding an MCP tool to an AI agent.

    **Note:** On the Model Context Protocol Server Console record, you will see a warning that server requires authentication.

9.  Select **Save** and continue to complete filling the Server details, Access rules, and Tools.

10. Verify the Server details.

    The Server name, Connection Alias, and Application fields are auto-populated with the information from previous steps. Additionally, you can provide a description for the server.

11. Define Security controls for the MCP Servers.

    For more information, see [Define security controls for MCP Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-mcp.md).

12. Define the Tools for the Model Context Protocol Sever.

    You can configure the MCP tools in the Assistant Designer. For more information see [Assign Model Context Protocol \(MCP\) servers to an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/assign-mcp-servers.md).

13. Select **Authenticate** to request a new token.

14. In the third-party authorization page, select **Authorize**.

    **Note:** When OAuth access or refresh tokens aren’t available, you must authenticate the OAuth configuration on the MCP server record to add it as an AI agent tool.


