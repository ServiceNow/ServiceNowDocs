---
title: Managing MCP server records
description: Learn about the MCP server record, including the MCP server overview and details available in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/managing-mcp-server-details.html
release: australia
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 4
breadcrumb: [Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Managing MCP server records

Learn about the MCP server record, including the MCP server overview and details available in AI Control Tower.

An MCP server record in AI Control Tower provides a detailed view of a registered MCP server. The record shows the server's identity, connectivity configuration, AI Gateway integration details, lifecycle stage, and risk and compliance posture. Use the record to monitor server health, manage authorization, and apply governance controls.

## MCP server Overview

When you select an MCP server from the inventory list, the MCP server record opens.

## Key details panel

The Key details panel on the Overview tab displays the primary identity and connectivity information for the MCP server. The following fields are available:

|Field|Description|
|-----|-----------|
|Asset tag|The unique ID assigned to this asset. Each asset tag consists of a type prefix followed by a 20-digit number.|
|Name|The display name of the MCP server as registered in AI Control Tower.|
|Description|A free-text description of the MCP server’s purpose, capabilities, or usage context.|
|Lifecycle phase|The current lifecycle stage of the MCP server. Reflects the phase selected during registration or updated through the Lifecycle tab.|
|Asset type|The classification of this record. Always MCP server for records of this type.|
|MCP server URL|The endpoint URL of the external MCP server. AI agents and the AI Gateway use this URL to connect to the server and call its tools. For example, https://mcp.linear.app/mcp.|
|External documentation URL|A link to the vendor-provided or internally authored documentation for this MCP server.|
|Provider|The organization or vendor that publishes or maintains this MCP server.|
|Business application|The ServiceNow business application that this MCP server is associated with. This field establishes ownership and CMDB relationships.|

## AI Gateway MCP server details panel

The AI Gateway MCP server details panel displays the ServiceNow-side connectivity configuration that the AI Gateway uses to proxy requests to and from the external MCP server.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Gateway MCP server URL

</td><td>

The internal ServiceNow URL through which the AI Gateway exposes this MCP server to the AI agents. AI agents send requests to this URL rather than directly to the external MCP Server URL.**Note:** The AI Gateway proxy URL format has changed. The new format is:

`https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

Previously, the URL format was:

`https://<instance-url>/sncapps/awh/<mcp-server>/mcp`

However, those who were using AI Gateway before the temporary unavailability in August will be redirected automatically to the latest URL.

</td></tr><tr><td>

Authorization endpoint URL

</td><td>

The OAuth 2.0 authorization endpoint used to initiate the authorization code flow for this MCP server. For example, https://&lt;instance&gt;.service-now.com/mcp\_auth.do

</td></tr><tr><td>

Token endpoint URL

</td><td>

The OAuth 2.0 token endpoint used to exchange authorization codes for access tokens. For example, https://&lt;instance&gt;.service-now.com/mcp\_token.do

</td></tr></tbody>
</table>## MCP server Details

The Details tab of an MCP server record displays the server’s governance metadata, ownership information, and the complete list of tools that the server exposes. Use this tab to review and update server details, manage attachments, and audit the tools available to AI agents through this server.

The tab is divided into two main panels displayed side by side:

-   Details panel
-   Available MCP tools panel

## Details panel

The Details panel displays the governance attributes and system-generated timestamps for the MCP server. These fields reflect the server’s current state in the AI Control Tower governance framework.

|Field|Description|
|-----|-----------|
|Name|The display name of the MCP server as registered in AI Control Tower.|
|Managed status|Indicates whether the MCP server is under active AI governance. Possible values are Managed and Unmanaged. A managed server is subject to approval workflows, policy enforcement, and audit logging.|
|Asset type|The classification of this record. Always MCP server for records of this type.|
|Managed by|The ServiceNow user responsible for governing this MCP server. This is the designated AI steward or asset owner.|
|State|The current lifecycle stage of the MCP server. For example: Deployed. Reflects the phase set during registration or updated through the Lifecycle tab.|
|Status|The approval status of the MCP server in the governance workflow.|
|Risk classification|The assessed risk level of the MCP server. For example: To be determined. This value remains as To be determined until a formal risk assessment is completed through the Risk &amp; compliance tab.|
|Created|The date and time the MCP server record was created in AI Control Tower. This field is system-generated and read-only.|
|Updated|The date and time the MCP server record was last modified. This field is system-generated and read-only.|

## Available MCP tools panel

The Available MCP tools panel, displayed to the right of the Details panel, lists tools that the MCP server exposes to AI agents. Each tool represents a discrete capability that an AI agent can invoke through the AI Gateway.

The panel shows the following columns:

|Column|Description|
|------|-----------|
|Name|The programmatic name of the tool as defined by the MCP server. Tool names use underscore-separated lowercase format, for example, get\_diff, create\_issue\_label.|
|Description|A natural-language description of the tool’s function and usage context. Descriptions are provided by the MCP server and reflect the vendor’s documentation.|
|Status|Indicates whether the tool is currently active and available for AI agents to call. Values are Active \(green\) and Inactive \(red\).|

## Tool Status

Each tool in the Available MCP tools panel has a status that indicates its operational availability:

|Status|Description|
|------|-----------|
|Active|The tool is operational and available for AI agents to invoke through the AI Gateway. Active tools appear with a green status badge.|
|Inactive|The tool is not available for use. AI agents can't invoke inactive tools. Inactive tools appear with a red badge. Contact your AI steward or MCP server administrator to investigate why the tool is inactive.|

