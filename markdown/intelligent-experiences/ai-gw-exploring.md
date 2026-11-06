---
title: Exploring AI Gateway
description: Learn how AI Gateway governs connections between AI agents and MCP servers, where you manage it, and how an MCP server is approved for agent traffic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-exploring.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, explore, AI Gateway, MCP server]
breadcrumb: [AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Exploring AI Gateway

Learn how AI Gateway governs connections between AI agents and MCP servers, where you manage it, and how an MCP server is approved for agent traffic.

## AI Gateway overview

When an agent connects to an MCP server directly, the agent holds the server's credentials, and you can't inspect or stop its traffic from one place. AI Gateway replaces those direct connections with a single governed endpoint for each server.

Agents send their requests to the server's AI Gateway MCP server URL, and AI Gateway forwards each call to the MCP server. On the way, AI Gateway is designed to perform three jobs:

-   **Govern**

    Agents can reach only MCP servers that are managed and approved, and only the tools that are active on each server. When access management is on for a server, each client is authorized to use only the tools that its client access policies grant through AI Gateway.

-   **Control**

    AI Gateway handles OAuth on both sides of the connection, so agents don't see the MCP server's credentials. It scans tools for threats, checks transactions for sensitive data, and lets you turn connections off for all servers or for one.

-   **Observe**

    AI Gateway records each call, so you can review activity for each server and tool.


## Where you manage AI Gateway

Settings that apply to every MCP server connection are on the AI Gateway settings page, at **Settings** &gt; **AI Gateway**. Each of its tabs is described in its own topic:

-   [AI Gateway Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-overview-tab.md)
-   [AI Gateway Tools tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-tools-tab.md)
-   [AI Gateway Policies tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-policies-tab.md)

Records opened from **Inventory** &gt; **Assets** &gt; **MCP servers** open on the **Overview** tab. Records opened by selecting a server name on the **Overview** tab of the settings page open on the **AI Gateway** tab, where per-server settings are. For the rest of the record, see [Working with MCP server records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/working-with-mcp-server-records.md).

## AI Gateway workflow

An MCP server goes through these stages before agents can call its tools through AI Gateway.

1.  The MCP server is added to the inventory. It can sync from AI Agent Studio, or an AI steward can add it from the MCP Catalog or AI Control Tower.
2.  The AI steward moves the server to managed, which starts the Onboard playbook on the record's **Lifecycle** tab.
3.  The AI steward completes the playbook's Assess, Build and Test, and Deploy phases. The record shows Deployed &amp; Approved, and its **AI Gateway** tab is ready for client registration.
4.  The AI steward registers the clients that can connect to the server.
5.  Optionally, the AI steward creates client access policies and turns on access management for the server, so that each client can use only the tools that it requires.
6.  Agent owners configure their agents to use the AI Gateway MCP server URL and the client credentials.
7.  The AI steward reviews the server's tools and policies, reviews its activity, and turns its connections off when needed.

## AI Gateway benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Allow agents to reach only MCP servers that an AI steward has assessed, tested, and approved.|[MCP server approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-mcp-server-approval-playbook-workflow.md)|AI steward|
|Keep MCP server credentials out of agent configurations. Agents authenticate with AI Gateway, and AI Gateway manages the credentials for the MCP server.|[Client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/client-registration.md)|AI steward, agent owners|
|Automatically deactivate tools that the security scan finds vulnerable.|[Tool automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-tools-tab.md)|AI steward|
|Help filter sensitive data, such as personally identifiable information \(PII\), in transactions between agents and MCP servers.|[Data Sensitivity Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-policies-tab.md)|AI steward|
|Limit each client to the tools that it requires on an MCP server.|[Client access policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md)|aig\_admin, AI steward|
|Stop traffic to every MCP server, or to one server, without changing any agent.|[Connection controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-connections.md)|AI steward|

## What to explore next

To learn more about configuring and using AI Gateway, see:

-   [Configuring AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-configuring.md)
-   [Connecting agents through AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-connecting-agents.md)
-   [Governing MCP server tools and data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-governing-tools-data.md)
-   [Controlling MCP server traffic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-traffic.md)
-   [AI Gateway reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-reference.md)

