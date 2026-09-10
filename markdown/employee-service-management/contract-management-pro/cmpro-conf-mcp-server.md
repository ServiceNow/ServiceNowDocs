---
title: Set up the Contract Management Pro MCP Server
description: Activate the Contract Management Pro MCP Server to enable contract analysis playbook driven document analysis and redlining.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-conf-mcp-server.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [MCP server, Contract Management Pro MCP Server, OAuth, Contract negotiation, Configure MCP server]
breadcrumb: [Configure Contract Management Pro MCP Server, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Set up the Contract Management Pro MCP Server

Activate the Contract Management Pro MCP Server to enable contract analysis playbook driven document analysis and redlining.

## Before you begin

The following plugins must be activated on your instance:

-   Model Context Protocol Server \(sn\_mcp\_server\)
-   Contract Management Pro MCP Server \(sn\_cm\_mcp\_server\)

For more information, see [Configure Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-install-mcp-app.md).

Role required: sn\_mcp\_server.admin or admin

## Procedure

1.  Navigate to **All** &gt; **MCP Server Console**.

2.  Change the application scope to **SN CMPro MCP Server**.

3.  From the **Configuration** tab, select **Servers**.\[Omitted image "cmpro-mcp-server-console.png"\] Alt text: MCP server console

4.  On the **SN CMPro MCP Server** card, select **Card actions** icon \( \[Omitted image "cmpro-mcp-srv-actions-icon.png"\] Alt text: Card actions icon\) and **Activate** if the MCP server is in deactivated state.

    \[Omitted image "cmpro-mcp-srv-activate.png"\] Alt text: Activate MCP server

    Activating the Contract Management Pro MCP Server automatically makes all the tools available to the connected MCP clients and creates an OAuth client entry with the Contract Management Pro MCP Server integration name, for example, **contracts\_mcp\_server**. For more information on the tools, see [Contract Management Pro MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-mcp-server-tools.md).

5.  Select **SN CMPro MCP Server**.

    \[Omitted image "cmpro-mcp-server-details.png"\] Alt text: SN CMPro MCP Server

6.  Set up OAuth to securely authenticate the Contract Management Pro MCP Server with your ServiceNow instance.

    **Note:** Change the application scope to **Global**.

<table id="choicetable_tss_d1b_dkc"><thead><tr><th align="left" id="d147935e227">

Authentication option

</th><th align="left" id="d147935e230">

Steps

</th></tr></thead><tbody><tr><td id="d147935e236">

**Use the Contract Management Pro MCP Server OAuth client entry**

</td><td>

1.  Select **Set up OAuth**.
2.  Navigate to the **contracts\_mcp\_server** client.

The fields on the Authorization code grant page are automatically populated.

3.  In the Provider name field, select **OAuth**.
4.  Select **Save**.


</td></tr><tr><td id="d147935e274">

**Set up your own OAuth connection**

</td><td>

See [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md) for the steps to set up the OAuth and connect to the Contract Management Pro MCP Server.

</td></tr></tbody>
</table>
## Result

The Contract Management Pro MCP Server is enabled and enforces OAuth 2.0 authentication. A connected AI tool that authenticates successfully and carries the sn\_cm\_gen\_ai.ai\_contract\_fulfiller role can call the playbook tool.

## What to do next

Create at least one active playbook for each contract type. For more information, see [Create a contract analysis playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-create-negotiation-playbook.md).

**Parent Topic:**[Configure Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-install-mcp-app.md)

