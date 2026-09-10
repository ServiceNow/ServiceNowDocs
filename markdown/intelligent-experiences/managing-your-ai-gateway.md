---
title: Managing your AI Gateway
description: Manage your AI Gateway tab on the MCP server record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/managing-your-ai-gateway.html
release: australia
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 3
breadcrumb: [Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Managing your AI Gateway

Manage your AI Gateway tab on the MCP server record.

The AI Gateway tab displays the configuration for exposing the MCP server to AI agents. Use the tab to review connectivity endpoints, manage MCP client integrations, configure available tools, and apply gateway policies to the server.

## AI Gateway in MCP server record

The AI Gateway acts as a managed proxy between AI agents and external MCP servers. When an AI agent needs to use tools from an MCP server, it connects through the AI Gateway rather than directly to the external server. This approach centralizes authentication, helps enforce policies, and provides observability for tool calls.

The AI Gateway tab provides a complete view of how a specific MCP server is integrated with the AI Gateway. It is divided into three sub-tabs:

|Sub-tab|Description|
|-------|-----------|
|Setup|Displays the AI Gateway MCP server connection details and the MCP clients integrated with this server. This is the default sub-tab.|
|Tools|Lists the tools exposed by this MCP server through the AI Gateway and allows tool-level configuration.|
|Policies|Lists the gateway policies applied to this MCP server, such as rate limiting, access control, and usage policies.|

## Setup

The Setup sub-tab is the default view of the AI Gateway tab. It displays the endpoints that clients and agents use to connect to this MCP server through the AI Gateway. It also lists the MCP clients registered to use this server.

**AI Gateway MCP server details panel**

The AI Gateway MCP server details panel displays the ServiceNow-generated endpoints that clients and agents use to connect to this MCP server through the AI Gateway.

**MCP client integration panel**

The MCP client integration panel lists all MCP clients registered to use this MCP server through the AI Gateway. The count badge next to the panel heading shows the total number of registered clients.

An MCP client is a consumer of the MCP server’s tools — typically an AI agent host application, a developer tool, or an integrated platform. MCP clients connect to the AI Gateway MCP server URL to invoke tools.

To register a client, select **Add client**. After registration, clients can be edited on the Edit Client page.

## Tools

The Tools sub-tab lists the tools exposed by the MCP server through the AI Gateway and allows tool-level configuration.

Before MCP server tools are activated, the system scans them to determine whether they pose a potential security threat. Threat categories are based on the OWASP MCP Top 10, the ten most critical MCP-related security vulnerabilities as defined by OWASP. For more information, see [OWASP MCP Top 10](https://owasp.org/www-project-mcp-top-10/).

System properties control whether Now Assist Guardian tool scanning and more advanced scanning are enabled. For more information, see [System properties for AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-reference-system-properties.md).

|Threat category|Description|
|---------------|-----------|
|credential\_harvesting|Potential collection or exposure of sensitive credentials.|
|excessive\_permissions|Optional parameters potentially granting dangerous capabilities beyond their stated purpose.|
|execution|Potential shell commands, code evaluation, or subprocess spawning.|
|exfiltration|Potential unauthorized data export to external destinations.|
|hidden\_instructions|Potentially concealed directives using steganography or authority-framing manipulation.|
|name\_description\_mismatch|Tool name potentially implies a different function than the description or schema reveals.|
|network|Potential unauthorized network access \(SSRF, DNS rebinding, or arbitrary URLs\).|
|none|No potential threats detected.|
|obfuscation|Encoded content \(base64, hex, URL-encoded\) potentially concealing true behavior.|
|prompt\_injection\_payload|Potential direct prompt injection. For example, a phrase such as "ignore all previous instructions".|
|tool\_poisoning|Description contains instructions that could potentially manipulate agent behavior.|
|write|Potential unauthorized file system modifications.|

Scan status indicates the current state of the MCP tool scan. Possible values are:

-   Completed
-   Failed
-   Pending
-   Timeout

## Policies

The Policies sub-tab lists the data governance policies applied to the server. From the Policies sub-tab, you can manage policy enforcement at the server level and the individual tool level.

**Data sensitivity check**

The Data sensitivity check area controls whether the AI Gateway inspects tool inputs and outputs for sensitive data. When enabled, this setting prevents sensitive data from passing between AI agents and the MCP server.

**Policy status table**

The policy card displays the current server-level state of the Data sensitivity check policy and provides a control to change it.

|Policy status|Description|
|-------------|-----------|
|Activated|The Data sensitivity check is enabled at the server level. The Deactivate button is available. Enforcement still depends on individual tool-level Policy status settings.|
|Deactivated|The Data sensitivity check is disabled at the server level. No sensitive data inspection occurs for any tool on this server, regardless of tool-level Policy status. Select Activate to turn it on.|

