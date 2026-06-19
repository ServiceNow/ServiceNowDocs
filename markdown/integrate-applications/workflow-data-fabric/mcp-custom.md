---
title: Client registration using custom connector
description: Define a custom connector by providing your own MCP endpoint URL and authentication configuration if the registry does not contain a connector for the system you need.Create an MCP Connector with OAuth 2.1 for connecting to external systems or applications that support MCP.Create an MCP Connector with API key for connecting to external systems or applications that support MCP.Create an MCP Connector with Basic Authentication for connecting to external systems or applications that support MCP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/mcp-custom.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 6
breadcrumb: [Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Client registration using custom connector

Define a custom connector by providing your own MCP endpoint URL and authentication configuration if the registry does not contain a connector for the system you need.

## Before you begin

Role required: wdf\_builder or admin.

## About this task

Use a custom connector in the following situations:

-   The third-party system exposes an MCP-compatible endpoint, but no certified or community connector exists in the registry for it.
-   You are connecting to an internal or proprietary system within your organization that is not listed in the registry.
-   You need to override the endpoint URL or authentication settings of an existing registry connector for a specific environment or configuration.

Custom connectors support both manual and dynamic client registration, depending on the capabilities of the target system. Custom connectors are scoped to the instance and are not added to the shared MCP registry.

## Create an MCP Connector with OAuth 2.1

Create an MCP Connector with OAuth 2.1 for connecting to external systems or applications that support MCP.

### Before you begin

Role required: sn\_mcp\_client.admin

### About this task

OAuth 2.1 provides the most secure and flexible authentication for MCP connectors. If your MCP server supports it, select OAuth 2.1 as the authentication method. You can choose between Dynamic Client Registration, where the server auto-populates client details, or Manual Client Registration, where you provide the client details yourself.

### Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click **Create** and select **Model Context Protocol**.

    The list of all available MCP connectors is displayed.

    \[Omitted image "custom-connector.jpg"\] Alt text:

3.  Click **Create a custom connector**.

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

Click the \[Omitted image "icon-plus.png"\] Alt text: Plus icon. icon to add an external system. For more information, see [Create external systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/connecthub-create-external-systems.md).**Note:** If you already have an existing system, you can use that system for the MCP connector.

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

    \[Omitted image "connect-hub-mcp-connector.png"\] Alt text: Example authorization request for Linear MCP connector

    You are redirected to the third-party page requesting authorization for the MCP client.

6.  Click **Approve**.

    The MCP client for your application is created and appears in the **Model Context Protocol** list.


## Create an MCP Connector with API Key

Create an MCP Connector with API key for connecting to external systems or applications that support MCP.

### Before you begin

Role required: sn\_mcp\_client.admin

### About this task

Use API key authentication when your MCP server requires a static key for authorization. Obtain the API key from your third-party application before configuring the connector.

### Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click **Create** and select **Model Context Protocol**.

    The list of all available MCP connectors is displayed.

    \[Omitted image "custom-connector.jpg"\] Alt text:

3.  Click **Create a custom connector**.

4.  On the form, fill in the fields.

<table id="table_system_details_apikey"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server name

</td><td>

Name of the MCP server. For example, *Figma MCP server*.

</td></tr><tr><td>

System

</td><td>

Search for the external system you want to integrate.

</td></tr><tr><td>

Add system \(Optional\)

</td><td>

Click the \[Omitted image "icon-plus.png"\] Alt text: Plus icon. icon to add an external system. For more information, see [Create external systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/connecthub-create-external-systems.md).**Note:** If you already have an existing system, you can use that system for the MCP connector.

</td></tr><tr><td>

Connection name

</td><td>

Select **New connection** and enter a name to uniquely identify the connection. For example, *Figma Connection*.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Endpoint name|This field is auto-populated with the Connection name.|
    |Endpoint URL|Connection URL for the MCP server.|
    |Authentication Method|Select **API key**.|
    |API key|Enter the API key of the third-party application.|

5.  Click **Save**.

    You are redirected to the third-party page requesting authorization for the MCP client.

6.  Click **Approve**.

    The MCP client for your application is created and appears in the **Model Context Protocol** list.


## Create an MCP Connector with Basic Authentication

Create an MCP Connector with Basic Authentication for connecting to external systems or applications that support MCP.

### Before you begin

Role required: sn\_mcp\_client.admin

### About this task

Use Basic Authentication when your MCP server requires a username and password for access. Ensure that valid server credentials are available before configuring the connector.

### Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub**.

2.  Click **Create** and select **Model Context Protocol**.

    The list of all available MCP connectors is displayed.

    \[Omitted image "custom-connector.jpg"\] Alt text:

3.  Click **Create a custom connector**.

4.  On the form, fill in the fields.

<table id="table_system_details_basicauth"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server name

</td><td>

Name of the MCP server. For example, *Figma MCP server*.

</td></tr><tr><td>

System

</td><td>

Search for the external system you want to integrate.

</td></tr><tr><td>

Add system \(Optional\)

</td><td>

Click the \[Omitted image "icon-plus.png"\] Alt text: Plus icon. icon to add an external system. For more information, see [Create external systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/connecthub-create-external-systems.md).**Note:** If you already have an existing system, you can use that system for the MCP connector.

</td></tr><tr><td>

Connection name

</td><td>

Select **New connection** and enter a name to uniquely identify the connection. For example, *Figma Connection*.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Endpoint name|This field is auto-populated with the Connection name.|
    |Endpoint URL|Connection URL for the MCP server.|
    |Authentication Method|Select **Basic Authentication**.|
    |User name|User name of the MCP server.|
    |Password|Password of the MCP server.|

5.  Click **Save**.

    You are redirected to the third-party page requesting authorization for the MCP client.

6.  Click **Approve**.

    The MCP client for your application is created and appears in the **Model Context Protocol** list.


