---
title: Governing MCP server tools and data
description: Review scan results for an MCP server's tools, decide which tools agents can call, and choose the tools that the Data Sensitivity Check applies to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-governing-tools-data.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, use, MCP tools, tool scan, Data Sensitivity Check]
breadcrumb: [AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Governing MCP server tools and data

Review scan results for an MCP server's tools, decide which tools agents can call, and choose the tools that the Data Sensitivity Check applies to.

## Overview of governing tools and data

The settings on the AI Gateway settings page apply to every MCP server connected through AI Gateway. To work with one server, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers**, select the server name, and then select the **AI Gateway** tab. While AI Gateway or the server's connection is paused, a warning appears and you can't change the server's tools or policies. The **Tools** and **Policies** sub-tabs apply to that server only. For a description of the tab, see [Managing your AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/managing-your-ai-gateway.md).

## Tools sub-tab

The **All tools** list shows every tool that the server exposes, with a count. Select **Refresh tools** to scan the server's tools again. If the server's authorization has expired, select **Reauthorize** first.

|Column|Description|
|------|-----------|
|Name|The tool's name, as defined by the MCP server.|
|Description|The tool's description, as provided by the MCP server.|
|Scan status|The result of the tool's security scan, such as Passed, Failed, or Safe.|
|Threat category|The type of threat that the scan found, or none.|
|Active|A toggle that controls whether agents can call the tool through AI Gateway, after you confirm. AI Gateway is set up to block every call to a tool when it's inactive. The toggle is unavailable while AI Gateway or the server's connection is paused.|

## Policies sub-tab

The **Policy categories** list shows **Data sensitivity**, with the number of policy types in the category. When client access control is on for the instance, the list starts with **Access management**, which opens by default and shows the number of client access policies on the server. For details, see [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md). When you select **Data sensitivity**, the **Data sensitivity check** card shows whether the policy is activated for the server and has a button to activate or deactivate it, after you confirm. The button is unavailable until the policy is activated for all servers on the AI Gateway settings page, and while connections are paused. To define what sensitive data is detected, select **Advanced settings**, which opens the Data Privacy configuration in a new browser tab.

The **Tools** list below the card shows each tool's **Policy status**, for example Active, with a button to deactivate or activate the policy for that tool. The buttons are unavailable until the policy is activated for the server, and each change asks you to confirm.

-   [Activate or deactivate a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-activate-tool.md): allow or block calls to one tool.
-   [Apply the Data Sensitivity Check to a server's tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-apply-dsc-tools.md): choose which of a server's tools the policy inspects.
-   [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md): limit each client to specific tools on a server.

