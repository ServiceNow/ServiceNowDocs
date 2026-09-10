---
title: Activate the ITOM MCP Server Console
description: Activate the ITOM MCP Server Console to enable AI-driven alert management capabilities on your ServiceNow instance through Model Context Protocol \(MCP\) connectivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/activate-itom-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [MCP Server, ITOM, OAuth, Model Context Protocol]
breadcrumb: [Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Activate the ITOM MCP Server Console

Activate the ITOM MCP Server Console to enable AI-driven alert management capabilities on your ServiceNow instance through Model Context Protocol \(MCP\) connectivity.

## Before you begin

Verify that the following plugins are installed on your instance:

-   ServiceNow Otto for IT Operations Management \(ITOM\) \(sn\_itom\_gen\_ai\)
-   Event Management \(com.glideapp.itom.snac\)
-   ITOM MCP Server Console \(sn\_itom\_mcp\_server\)
-   Model Context Protocol Server \(sn\_mcp\_server\)

To use the Alert Hypothesizer described in [Investigate alerts using an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/review-alerts-using-itom-mcp-server.md), you must also install Health Log Analytics plugin.

To use the CI reliability and SLO tools described in [Review CI reliability with an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/review-ci-reliability-itom-mcp-server.md), you must also have the following plugins installed:

-   Service Reliability Management \(sn\_sow\_srm\)
-   Service Level Objective Management \(sn\_sow\_slo\)
-   AI agents for SLO \(sn\_ai\_agents\_slo\)

Refer to [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md) for more information about setting up the OAuth and connecting to the MCP Server Console.

Role required: sn\_mcp\_server.admin

**Note:** To set up your own OAuth connection, you need either an oauth\_admin, or admin role to configure your OAuth client entry.

## Procedure

1.  Activate the ITOM MCP Server Console.

    1.  Navigate to **All** &gt; **MCP Server Console**.

    2.  From the Configuration tab, select **Servers**.

    3.  Select the **ITOM MCP Server**.

        **Note:** You must change the application scope to **ITOM MCP Server**

        The **MCP Server Console** screen opens with all fields populated. \[Omitted image "itom-mcp-server-console.png"\] Alt text: ITOM MCP Server configuration details page

    4.  From the Deactivate drop-down menu, select **Activate**.

2.  Set up OAuth to securely authenticate the ITOM MCP Server Console with your ServiceNow instance.

    Refer to the instructions in [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md) to setup the OAuth and connect to the MCP Server Console.

    **Note:** To set up your own OAuth connection, you need either an oauth\_admin, or admin role to configure your OAuth client entry.


**Related topics**  


[MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mcp-platform-manager-landing.md)

[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-mcp-server-console.md)

[Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md)

[Install Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-mcp-client.md)

