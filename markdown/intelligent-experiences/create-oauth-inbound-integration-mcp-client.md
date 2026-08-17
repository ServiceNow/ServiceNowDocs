---
title: Create an OAuth inbound integration for an MCP client
description: Secure access to Model Context Protocol \(MCP\) servers on an instance by creating an OAuth inbound integration for each MCP client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-oauth-inbound-integration-mcp-client.html
release: zurich
topic_type: task
last_updated: "2025-11-12"
reading_time_minutes: 2
breadcrumb: [Connect, MCP Server Console, Enable AI experiences]
---

# Create an OAuth inbound integration for an MCP client

Secure access to Model Context Protocol \(MCP\) servers on an instance by creating an OAuth inbound integration for each MCP client.

## Before you begin

Role required: oauth\_admin, mi\_admin, admin

## About this task

For each client that you want to access servers on an instance, create an OAuth inbound integration in Machine Identity Console. To create the OAuth integration, you need a redirect URL from the client. For more information, refer to the documentation for your AI application and client.

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  From the Configuration tab, select **Servers**.

3.  From the OAuth setup required banner, select **Set up OAuth**.

    Alternatively, you can navigate to **All** &gt; **Machine Identity Console** and select the **Inbound integrations** tab.

    **Note:** In the list of existing inbound integrations, you might see integrations created with the same names as servers \(including underscores\). These are integrations for monitoring servers from AI Control Tower and shouldn't be used to integrate with clients.

4.  Select **New integration**.

5.  Select **OAuth - Authorization code grant**.

6.  On the form, fill in the required fields.

    For more information about this form, see [Configure an OAuth authorization code grant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/configure-an-oauth-authorization-code-grant.md).

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

Enter the redirect URL for a client. The authorization code is sent to this URL after authentication. To get the redirect URL, refer to the documentation for your AI application and client.To connect to the ServiceNow MCP client on another instance, use the following redirect URL: `https://<client-instance>.service-now.com/oauth_redirect.do`. For more information, see the [Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mcp-client.md) documentation.

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

    \[Omitted image "mcp-server-oauth-inbound-integration.png"\] Alt text: An OAuth inbound integration for Claude to connect to MCP servers as an MCP client.


## What to do next

Configure the client to use the client ID and client secret to authenticate with servers on the instance.

-   **[Create client authorizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-client-authorizations.md)**  
Establish connections between your MCP clients and servers with client authorizations.

**Parent Topic:**[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/connect-mcp-server-client.md)

