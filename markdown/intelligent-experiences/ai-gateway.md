---
title: AI Gateway
description: Use the AI Gateway settings page to control global transaction processing for all connected MCP servers and manage individual MCP server connections independently of the global gateway state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-gateway.html
release: zurich
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 3
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# AI Gateway

Use the AI Gateway settings page to control global transaction processing for all connected MCP servers and manage individual MCP server connections independently of the global gateway state.

Role required: sn\_ai\_governance.ai\_steward

The AI Gateway settings page is the administrative control center for the AI Gateway in AI Control Tower. From this page, you can:

-   Pause or resume global transaction processing across all MCP servers simultaneously.
-   Monitor the connection status of individual MCP servers in real time.
-   Pause or resume traffic to specific MCP servers independently from the global setting.
-   Configure tools and policies for the AI Gateway using the Tools and Policies tabs.

The page is organized into three tabs: Overview, Tools, and Policies.

## Overview tab

The Overview tab displays the global transaction control banner and the MCP servers list with server name, connection status, and server-level pause controls.

The transaction status banner appears at the top of the Overview tab. It shows the current global state of AI Gateway transaction processing and provides a control to change that state.

**MCP servers table**

The MCP servers section lists all MCP servers registered with the AI Gateway. The section header displays the total count of registered servers. The table provides the following columns for each server.

<table id="table_o43_ynd_kjc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server name

</td><td>

The display name of the MCP server as registered in the AI Gateway. The name links to the server's inventory record in AI Control Tower.

</td></tr><tr><td>

Connection status

</td><td>

Connection state, shown as a color-coded dot and label:-   Green: Server is actively connected and processing requests.
-   Red: Server is not reachable or has been paused.

</td></tr><tr><td>

Last updated

</td><td>

The date and time when the connection status was last refreshed for this server.

</td></tr><tr><td>

Pause / Resume button

</td><td>

Controls traffic to this MCP server. Select Pause to stop the AI Gateway from routing requests to this server only. Other servers continue to operate normally. Select Resume to restore routing.

</td></tr></tbody>
</table>## Tools tab

The Tools tab governs the lifecycle of individual tools exposed by MCP servers. It provides two global toggle settings that automate tool management decisions based on security scanning results and MCP server approval workflows.

**Tools tab settings**

The Tools tab displays two configurable toggle settings: Auto-deactivate vulnerable tools and Auto-activate new tools. Both toggle settings are enabled by default.

|Toggle settings|Description|
|---------------|-----------|
|Auto-deactivate vulnerable tools|New tools are automatically activated when an MCP server is approved. Tools identified as vulnerable are automatically deactivated.|
|Auto-activate new tools|New tools are automatically activated. Vulnerable tools are flagged but remain active until manually deactivated.|

## Policies tab

The Policies tab lets you manage how built-in AI Gateway policies are enforced across registered MCP servers. Each policy in AI Gateway targets a specific type of governance — such as data sensitivity checking — and can be applied selectively to individual servers.

From the Policies tab, you can view which MCP servers are running under a given policy and monitor their enforcement status. You can also activate or deactivate policy enforcement per server without affecting the global policy state.

**AI Gateway policy**

AI Gateway policy defines a set of rules that AI Control Tower can enforce when AI agents interact with MCP servers through the gateway. Policies operate at the server level: you can enable a policy for one server while leaving it inactive for another. AI Control Tower includes the following built-in policy:

Data Sensitivity Check: Scans tool inputs and outputs for sensitive data types. When active, the policy can intercept agent interactions and block or flag content that matches the configured sensitivity rules.

The Policies tab is organized into two areas: a policy activation banner and a server list.

The banner at the top of the page shows whether the policy is currently activated at the global level. It provides the following controls:

-   Activate / Deactivate — Turns the policy on or off globally. When deactivated, the policy is not enforced for any server regardless of individual server policy status.
-   Configure sensitive data types — A link that opens the sensitive data type configuration page, where you define the data categories the policy detects.

The server list displays all MCP servers that are associated with the active policy. The list includes the following columns:

|Column|Description|
|------|-----------|
|Server name|The name of the MCP server running under the policy. Select the server name to view its details.|
|Policy status|Indicates whether the Data Sensitivity Check policy is enforced for this server. When active, the server enforces the policy. When inactive, the server does not.|
|Action|Select Activate or Deactivate to change the policy enforcement status for this server.|

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring.md)

