---
title: Connecting to an MCP server from an MCP client
description: Connect to a Model Context Protocol \(MCP\) server from an MCP client by creating an OAuth inbound integration and configuring the client with the server details.Secure access to Model Context Protocol \(MCP\) servers on an instance by creating an OAuth inbound integration for each MCP client.Configure a Model Context Protocol \(MCP\) client to connect to an MCP server and prompt the server to perform a task.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [use]
breadcrumb: [MCP Server Console, Enable AI experiences]
---

# Connecting to an MCP server from an MCP client

Connect to a Model Context Protocol \(MCP\) server from an MCP client by creating an OAuth inbound integration and configuring the client with the server details.

With the Quickstart Server or after creating a server, you can complete the following steps to connect to a server from a client:

1.  [Create an OAuth inbound integration for an MCP client](connect-mcp-server-client.md#)
2.  [Configure an MCP client to connect to an MCP server](connect-mcp-server-client.md#)

The process to configure a client to connect to a server is dependent on the client used. For more information, refer to the documentation for your AI application and client.

## Create an OAuth inbound integration for an MCP client

Secure access to Model Context Protocol \(MCP\) servers on an instance by creating an OAuth inbound integration for each MCP client.

### Before you begin

Role required: oauth\_admin, mi\_admin, admin

### About this task

For each client that you want to access servers on an instance, create an OAuth inbound integration in Machine Identity Console. To create the OAuth integration, you need a redirect URL from the client. For more information, refer to the documentation for your AI application and client.

### Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Servers**.

3.  From the OAuth setup required banner, select **Set up OAuth**.

    Alternatively, you can navigate to **All** &gt; **Machine Identity Console** and select the **Inbound integrations** tab.

    **Note:** In the list of existing inbound integrations, you might see integrations created with the same names as servers \(including underscores\). These are integrations for monitoring servers from AI Control Tower and shouldn't be used to integrate with clients.

4.  Select **New integration**.

5.  Select **OAuth - Authorization code grant**.

6.  On the form, fill in the required fields.

    For more information about this form, see Configure an OAuth authorization code grant.

<table id="table_acq_zq2_hhc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr class="sub-head"><td colspan="2">

Details section

</td></tr><tr><td>

Name

</td><td>

Enter a name for the OAuth integration.

</td></tr><tr><td>

Redirect URLs

</td><td>

Enter the redirect URL for a client. The authorization code is sent to this URL after authentication. To get the redirect URL, refer to the documentation for your AI application and client.To connect to the ServiceNow MCP client on another instance, use the following redirect URL: `https://<client-instance>.service-now.com/oauth_redirect.do`. For more information, see the [Model Context Protocol Client](../../model-context-protocol-client/reference/mcp-client.md) documentation.

</td></tr><tr class="sub-head"><td colspan="2">

Auth scope section

</td></tr><tr><td>

Allow access only to APIs in selected scope

</td><td>

Clear the check box to make the OAuth integration broadly scoped.

</td></tr><tr class="sub-head"><td colspan="2">

Advanced options section

</td></tr><tr><td>

Token Format

</td><td>

Select **JWT**.

</td></tr></tbody>
</table>7.  Select **Save**.

    The OAuth inbound integration is created as broadly scoped with a client ID and client secret that you use when configuring the client to connect to servers on the instance.

    ![An OAuth inbound integration for Claude to connect to MCP servers as an MCP client.](../image/mcp-server-oauth-inbound-integration.png)


### What to do next

Configure the client to use the client ID and client secret to authenticate with servers on the instance.

## Configure an MCP client to connect to an MCP server

Configure a Model Context Protocol \(MCP\) client to connect to an MCP server and prompt the server to perform a task.

### Before you begin

Role required: none

### About this task

The process to configure a client to connect to a server is dependent on the client used. The following procedure is a high-level overview of the workflow to configure a client to call a server. For more information, refer to the documentation for your AI application and client. For an example that demonstrates how to connect from a server on one instance to the ServiceNow Model Context Protocol Client on another instance, see the example following this procedure.

### Procedure

1.  Configure a client with the required server details as determined by the client.

<table id="table_btb_gvf_hhc"><thead><tr><th>

Server details

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Server URL

</td><td>

`https://<server-instance>.service-now.com/sncapps/mcp-server/mcp/<server-name>`To connect to the preconfigured Quickstart Server, use `https://<server-instance>.service-now.com/sncapps/mcp-server/mcp/sn_mcp_server_default`.

</td></tr><tr><td>

Host

</td><td>

`<server-instance>.service-now.com`

</td></tr><tr><td>

Base URL

</td><td>

`/sncapps/mcp-server`

</td></tr><tr><td>

Scope

</td><td>

mcp\_server

</td></tr><tr><td>

Authentication type

</td><td>

OAuth 2.0

</td></tr><tr><td>

Identity Provider

</td><td>

Generic OAuth 2

</td></tr><tr><td>

Authorization URL

</td><td>

`https://<server-instance>.service-now.com/oauth_auth.do`

</td></tr><tr><td>

Token URL

</td><td>

`https://<server-instance>.service-now.com/oauth_token.do`

</td></tr><tr><td>

Token Revocation URL

</td><td>

`https://<server-instance>.service-now.com/oauth_revoke.do`

</td></tr><tr><td>

Refresh URL

</td><td>

`https://<server-instance>.service-now.com/oauth_auth.do`

</td></tr><tr><td>

Redirect URL

</td><td>

`https://<server-instance>.service-now.com/oauth/callback`

</td></tr><tr><td>

Client ID

</td><td>

The client ID from the OAuth inbound integration on the server instance.

</td></tr><tr><td>

Client secret

</td><td>

The client secret from the OAuth inbound integration on the server instance.

</td></tr></tbody>
</table>    After configuring these details, the client calls the server with the `Authorization: Bearer <token>` header. If the token is validated by the server, the client receives the list of tools available for use.

2.  From the client, you can view the list of tools available to determine how to prompt the server.

3.  Enter a prompt for the information you need or for the tool to perform an action on the instance.

    For example, if the Look up Incident Records tool is available, you could enter "Get all open incidents." With the Case summarization tool, you could enter "Summarize all cases closed this week."

    The server runs the relevant tools and returns the result to the client as JSON data. The client presents the response as formatted text.


### Connecting to an MCP server from ServiceNow Model Context Protocol Client

This example demonstrates how to connect to a server from an AI agent on another instance using the ServiceNow Model Context Protocol Client. First, you configure the client to call the preconfigured Quickstart Server. From an AI agent, you access the Quickstart Server's list of tools and add individual tools to the agent. Lastly, you test the agent in AI Agent Studio by providing a prompt and seeing the agent's response. For more information, see the [Model Context Protocol Client](../../model-context-protocol-client/reference/mcp-client.md) documentation.

Role required: sn\_mcp\_client.admin

1.  On the server instance, create an OAuth inbound integration for the ServiceNow Model Context Protocol Client.

    For more information, see [Create an OAuth inbound integration for an MCP client](connect-mcp-server-client.md#).

2.  On the client instance, navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.
3.  Select **Manage MCP Servers**.
4.  Select **New**.
5.  Add the Quickstart Server.

    For more information about this step, see [Add an MCP Server with OAuth 2.1](../../model-context-protocol-client/task/add-an-oauth-2-1-mcp-server.md).

    1.  On the Add MCP server form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|Quickstart Server|
        |Authentication Type|OAuth 2.1|
        |MCP server URL|`https://<server-instance>.service-now.com/sncapps/mcp-server/mcp/sn_mcp_server_default`|

    2.  Select **Next**.
    3.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Client registration type|Manual Registration|
        |Grant type|Authorization Code|
        |Token authentication method|Client Secret Post|
        |Client ID|The client ID from the OAuth inbound integration for the Model Context Protocol Client on the server instance.|
        |Client secret|The client secret from the OAuth inbound integration for the Model Context Protocol Client on the server instance.|
        |Authorization URL|`https://<server-instance>.service-now.com/oauth_auth.do`|
        |Token URL|`https://<server-instance>.service-now.com/oauth_token.do`|
        |Token Revocation URL|`https://<server-instance>.service-now.com/oauth_revoke.do`|

    4.  Select **Save**.
6.  Verify the OAuth configuration.
    1.  Select **Authenticate**.
    2.  Select **Allow** to allow the client to connect to the server.
7.  Add tools from the Quickstart Server to an AI agent.

    For more information about this step, see [Add an MCP server tool to an AI agent](../../model-context-protocol-client/task/add-mcp-server-tool.md).

    1.  In AI Agent Studio, select the **Create and manage** tab.
    2.  From the AI agents tab, select an existing agent or create one.

        For information about creating an agent, see [Create an AI agent](../../now-assist-ai-agents/task/configure-next-best-action-agent.md).

    3.  Select **Add tools and information**.
    4.  Select **Add tool** &gt; **MCP server tool**.
    5.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Select Model Context Protocol server|Quickstart Server|
        |Select tool|Select the tools from the Quickstart Server that you want to use with this AI agent.|

        ![Viewing the tools list for the Quickstart Server from an AI agent in AI Agent Studio.](../image/mcp-server-tools-list.png)

    6.  Select **Add**.
    7.  Select **Save and continue**.
8.  Test the AI agent.

    For more information about this step, see [Test an AI agent](../../model-context-protocol-client/task/test-ai-agent-mcp.md).

    1.  In AI Agent Studio, select the **Testing** tab.
    2.  Select **Start manual test**.
    3.  In the Choose a test type field, select **AI agent or workflow**.
    4.  Select the AI agent you configured and its version.
    5.  In the Task field, enter a prompt to get information or to perform an action on the instance.

        The prompt should be based on which tools are available. For example, if you added the Look up Case Records and Case summarization tools, you can enter "Summarize all cases closed this week."

        ![Prompting the AI agent for summaries of cases closed by Abel Tuter this week.](../image/mcp-server-prompt-agent.png)

    6.  Select **Continue to Test Chat Response**.
    The AI agent calls the server, and the server runs the tools requested based on the prompt. The server returns the information to the agent as JSON data, and the agent presents it as formatted text. In this example, the agent returns summaries of the cases closed by Abel Tuter in the past week.

    ![The agent responds with summaries of two cases closed by Abel Tuter this week.](../image/mcp-server-agent-response.png)


