---
title: Configure the HRSD MCP Server Console
description: Activate the HRSD MCP Server to enable AI-driven case management and employee experience on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/configure-hrsd-mcp-server.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 1
keywords: [MCP Server, HRSD, Integration, OAuth, AI integration, Model Context Protocol]
breadcrumb: [HRSD MCP Server, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure the HRSD MCP Server Console

Activate the HRSD MCP Server to enable AI-driven case management and employee experience on your ServiceNow instance.

## About this task

## Before you begin

The following plugins must be activated on your instance:

-   ServiceNow Otto for HR Service Delivery \(HRSD\) plugin \(sn\_hrsd\_gen\_ai\)
-   Model Context Protocol Server \(sn\_mcp\_server\)
-   HRSD MCP Server \(sn\_hrsd\_mcp\_server\)

Role required: sn\_mcp\_server.admin or admin

## Procedure

1.  Activate the HRSD MCP Server.

    1.  Navigate to **All** &gt; **MCP Server Console**.

    2.  From the **Configuration** tab, select **Servers**.

    3.  Select the **HRSD MCP Server**.

        **Note:** Change the application scope to **HRSD MCP Server**.

        The **MCP Server Console** page opens with all fields populated by default.

        \[Omitted image "hrsd-mcp-server-console.png"\] Alt text: HRSD MCP server Oauth access

    4.  Select **Activate**.

        Activating the HRSD MCP server automatically makes all the tools available to the connected MCP clients. For more information on the tools, see [MCP Server Tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/mcp-server-tools-reference.md).

        **Note:** Activating the HRSD MCP server creates an OAuth client entry with the HRSD MCP Server integration name, for example, **sn\_hr\_mcp\_server.hr\_default**.

2.  Set up OAuth to securely authenticate the HRSD MCP Server with your ServiceNow instance.

    **Note:** Change the application scope to **Global**.

<table id="choicetable_tss_d1b_dkc"><thead><tr><th align="left" id="d796783e208">

Authentication option

</th><th align="left" id="d796783e211">

Steps

</th></tr></thead><tbody><tr><td id="d796783e217">

**Use the HRSD MCP Server OAuth client entry**

</td><td>

1.  Select **Set up OAuth**.
2.  Navigate to the **sn\_hr\_mcp\_server.hr\_default** client.

The fields on the Authorization code grant page are automatically populated.

3.  In the Provider name field, select **OAuth**.
4.  Select **Save**.


</td></tr><tr><td id="d796783e255">

**Set up your own OAuth connection**

</td><td>

See [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md) for the steps to set up the OAuth and connect to the HRSD MCP Server.

</td></tr></tbody>
</table>
