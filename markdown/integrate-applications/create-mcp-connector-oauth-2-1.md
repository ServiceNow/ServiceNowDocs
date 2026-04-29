---
title: Create an MCP Connector with OAuth 2.1
description: Create an MCP Connector with OAuth 2.1 for connecting to external systems or applications that support MCP.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Create an MCP Connector with OAuth 2.1

Create an MCP Connector with OAuth 2.1 for connecting to external systems or applications that support MCP.

## Before you begin

Role required: sn\_mcp\_client.admin

## About this task

OAuth 2.1 provides the most secure and flexible authentication for MCP connectors. If your MCP server supports it, select OAuth 2.1 as the authentication method. You can choose between Dynamic Client Registration, where the server auto-populates client details, or Manual Client Registration, where you provide the client details yourself.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Select **Connectors**.

3.  Click **Create** and select **Model Context Protocol Connector**.

4.  On the form, fill in the fields.

<table id="table_system_details_oauth"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server name

</td><td>

Name of the MCP server. For example, *Linear MCP server*.

</td></tr><tr><td>

System

</td><td>

Search for the external system you want to integrate.

</td></tr><tr><td>

Add system \(Optional\)

</td><td>

Click the ![Plus icon.](../../../product/rpa-hub/image/icon-plus.png) icon to add an external system. For more information, see [Create external systems](../../../build/workflow-data-fabric/task/connecthub-create-external-systems.md#).**Note:** If you already have an existing system, you can use that system for the MCP connector.

</td></tr><tr><td>

Connection name

</td><td>

Select **New connection** and enter a name to uniquely identify the connection. For example, *Linear Connection*.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Endpoint name|This field is auto-populated with the Connection name.|
    |Endpoint URL|Connection URL for the MCP server.|
    |Authentication Method|Select **OAuth 2.1**.|

    Select the registration type based on your MCP server's capabilities.

<table id="table_manual_client_registration_oauth"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorization method

</td><td>

Select the grant type to be used for requesting tokens from the authorization server.-   **Authorization Code**: A system-generated code used for granting access to an application or resource.
-   **Client Credentials**: Access token provided by the administrator to access the application directly.


</td></tr><tr><td>

Client ID

</td><td>

Client ID of the OAuth provider.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of the OAuth provider.

</td></tr><tr><td>

Client Authentication

</td><td>

Specifies how the client credentials are sent to the OAuth token endpoint when requesting an access token.-   **Client Secret Post**: Sends the client ID and client secret in the request body as form-encoded parameters when calling the token endpoint.
-   **Client Secret Basic**: Sends the client ID and client secret in the HTTP Authorization header using Basic authentication when calling the token endpoint.


</td></tr><tr><td>

Access permissions

</td><td>

Select the required scopes. These scopes determine the permissions of this OAuth client.

</td></tr><tr><td>

OAuth Auth URL

</td><td>

URL of the OAuth authorization server.

</td></tr><tr><td>

OAuth Token URL

</td><td>

OAuth server endpoint used to obtain access tokens.

</td></tr><tr><td>

Token revocation URL

</td><td>

OAuth server endpoint used to revoke previously issued tokens.

</td></tr></tbody>
</table><table id="table_dynamic_client_registration_oauth"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorization method

</td><td>

Select the grant type to be used for requesting tokens from the authorization server.-   **Authorization Code**: A system-generated code used for granting access to an application or resource.
-   **Client Credentials**: Access token provided by the administrator to access the application directly.


</td></tr><tr><td>

Client Authentication

</td><td>

Select how the client credentials are sent when requesting tokens from the authorization server.-   **Basic Authorization Header**
-   **Request Body Parameter**
-   **Private Key Jwt**


</td></tr><tr><td>

Access permissions

</td><td>

Select the required scopes. These scopes determine the permissions of this OAuth client.

</td></tr><tr><td>

Authorization URL

</td><td>

URL of the OAuth authorization server.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server endpoint used to obtain access tokens.

</td></tr><tr><td>

Token revocation URL

</td><td>

OAuth server endpoint used to revoke previously issued tokens.

</td></tr><tr><td>

Client registration token

</td><td>

Token used to authenticate requests to the OAuth client registration endpoint.

</td></tr><tr><td>

Value

</td><td>

Token for dynamic client registration. Leave this value blank if the server supports unauthenticated registration.

</td></tr></tbody>
</table>5.  Click **Save**.

    For example:

    ![Example authorization request for Linear MCP connector](../image/connect-hub-mcp-connector.png)

    You are redirected to the third-party page requesting authorization for the MCP client.

6.  Click **Approve**.

    The MCP client for your application is created and appears in the **Model Context Protocol** list.


