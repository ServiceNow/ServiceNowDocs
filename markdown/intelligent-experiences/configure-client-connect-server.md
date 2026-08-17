---
title: Configure an MCP client to connect to an MCP server
description: Configure a Model Context Protocol \(MCP\) client to connect to an MCP server and prompt the server to perform a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/configure-client-connect-server.html
release: zurich
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 5
breadcrumb: [Connect, MCP Server Console, Enable AI experiences]
---

# Configure an MCP client to connect to an MCP server

Configure a Model Context Protocol \(MCP\) client to connect to an MCP server and prompt the server to perform a task.

## Before you begin

Role required: none

## About this task

The process to configure a client to connect to a server is dependent on the client used. The following procedure is a high-level overview of the workflow to configure a client to call a server. For more information, refer to the documentation for your AI application and client. For an example that demonstrates how to connect from a server on one instance to the ServiceNow Model Context Protocol Client on another instance, see the example following this procedure.

## Procedure

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


## Connecting to an MCP server from ServiceNow Model Context Protocol Client

This example demonstrates how to connect to a server from an AI agent on another instance using the ServiceNow Model Context Protocol Client. First, you configure the client to call the preconfigured Quickstart Server. From an AI agent, you access the Quickstart Server's list of tools and add individual tools to the agent. Lastly, you test the agent in AI Agent Studio by providing a prompt and seeing the agent's response. For more information, see the [Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mcp-client.md) documentation.

Role required: sn\_mcp\_client.admin

1.  On the server instance, create an OAuth inbound integration for the ServiceNow Model Context Protocol Client.

    For more information, see [Create an OAuth inbound integration for an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-oauth-inbound-integration-mcp-client.md).

2.  On the client instance, navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.
3.  Select **Manage MCP Servers**.
4.  Select **New**.
5.  Add the Quickstart Server.

    For more information about this step, see [Add an MCP server with OAuth 2.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/add-an-oauth-2-1-mcp-server.md).

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

    For more information about this step, see [Add an MCP server tool to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/add-mcp-server-tool.md).

    1.  In AI Agent Studio, select the **Create and manage** tab.
    2.  From the AI agents tab, select an existing agent or create one.

        For information about creating an agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-next-best-action-agent.md).

    3.  Select **Add tools and information**.
    4.  Select **Add tool** &gt; **MCP server tool**.
    5.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Select Model Context Protocol server|Quickstart Server|
        |Select tool|Select the tools from the Quickstart Server that you want to use with this AI agent.|

        \[Omitted image "mcp-server-tools-list.png"\] Alt text: Viewing the tools list for the Quickstart Server from an AI agent in AI Agent Studio.

    6.  Select **Add**.
    7.  Select **Save and continue**.
8.  Test the AI agent.

    For more information about this step, see [Test an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/test-ai-agent-mcp.md).

    1.  In AI Agent Studio, select the **Testing** tab.
    2.  Select **Start manual test**.
    3.  In the Choose a test type field, select **AI agent or workflow**.
    4.  Select the AI agent you configured and its version.
    5.  In the Task field, enter a prompt to get information or to perform an action on the instance.

        The prompt should be based on which tools are available. For example, if you added the Look up Case Records and Case summarization tools, you can enter "Summarize all cases closed this week."

        \[Omitted image "mcp-server-prompt-agent.png"\] Alt text: Prompting the AI agent for summaries of cases closed by Abel Tuter this week.

    6.  Select **Continue to Test Chat Response**.
    The AI agent calls the server, and the server runs the tools requested based on the prompt. The server returns the information to the agent as JSON data, and the agent presents it as formatted text. In this example, the agent returns summaries of the cases closed by Abel Tuter in the past week.

    \[Omitted image "mcp-server-agent-response.png"\] Alt text: The agent responds with summaries of two cases closed by Abel Tuter this week.


**Parent Topic:**[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-server-client.md)

