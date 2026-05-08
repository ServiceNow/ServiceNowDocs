---
title: Activate the ITOM MCP server
description: Activate the ITOM MCP Server to enable AI-driven alert management capabilities on your ServiceNow instance through Model Context Protocol \(MCP\) connectivity.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [MCP Server, ITOM, OAuth, Model Context Protocol]
breadcrumb: [Use the ITOM MCP Server, Now Assist for ITOM, IT Operations Management]
---

# Activate the ITOM MCP server

Activate the ITOM MCP Server to enable AI-driven alert management capabilities on your ServiceNow instance through Model Context Protocol \(MCP\) connectivity.

## Before you begin

Role required: sn\_mcp\_server.admin

You must have the following plugins installed on your instance:

-   Now Assist for IT Operations Management \(ITOM\) \(sn\_itom\_gen\_ai\)
-   Event Management \(com.glideapp.itom.snac\)
-   Model Context Protocol Server \(sn\_mcp\_server\)

To use the Alert Hypothesizer described in [Analyze alerts using the ITOM MCP Server with MCP client applications](review-alerts-using-itom-mcp-server.md), you must also install Health Log Analytics plugin.

To use the CI reliability and SLO tools described in [Review CI reliability with the ITOM MCP Server](review-ci-reliability-itom-mcp-server.md), you must also have the following plugins installed:

-   Service Reliability Management \(sn\_sow\_srm\)
-   Service Level Objective Management \(sn\_sow\_slo\)
-   AI agents for SLO \(sn\_ai\_agents\_slo\)

## Procedure

1.  Activate the ITOM MCP Server.

    1.  Navigate to **All** &gt; **MCP Server Console**.

    2.  From the Configuration tab, select **Servers**.

    3.  Select the **ITOM MCP Server**.

        **Note:** You must change the application scope to **Alert Assist**

        The **MCP Server Console** screen opens with all fields populated. ![ITOM MCP Server configuration details page](../image/itom-mcp-server-console.png)

    4.  From the Deactivate drop-down menu, select **Activate**.

2.  Set up OAuth to securely authenticate the ITOM MCP Server with your ServiceNow instance.

    Refer to the instructions in Connecting to an MCP server from an MCP client to setup the OAuth and connect to the MCP Server.

    **Note:** To set up your own OAuth connection, you need either an oauth\_admin, or admin role to configure your OAuth client entry.


**Related topics**  


[bundle-platai.mcp-server-console-landing]

[bundle-platai.configuring-mcp-server-console]

[bundle-platai.connect-mcp-server-client]

[bundle-platai.install-mcp-client]

