---
title: Configuring AI Gateway
description: Prepare your instance for AI Gateway, bring MCP servers into the inventory and approve them, and choose the settings that apply to your MCP server connections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-configuring.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, configure, AI Gateway, AI Gateway settings]
breadcrumb: [AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configuring AI Gateway

Prepare your instance for AI Gateway, bring MCP servers into the inventory and approve them, and choose the settings that apply to your MCP server connections.

## Configuration overview

1.  [Activating AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-activating.md)

    Activate AI Control Tower, which installs the AWH for AI Control Tower plugin \(sn\_awh\_config\) that provides AI Gateway. There's no separate plugin to activate. AI Gateway isn't available on instances that use domain separation. For information about domain separation in AI Control Tower, see [Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-domain-separation.md).

2.  [Configure users and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-users-and-roles.md)

    Give the people who manage AI Gateway the AI Steward \[sn\_ai\_governance.ai\_steward\] role.

3.  [MCP server setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mcp-server-setup.md)

    Add the MCP servers that agents use to the inventory. Servers that you add in AI Agent Studio sync to the inventory automatically.

4.  [MCP server approval playbook workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-mcp-server-approval-playbook-workflow.md)

    Move each server to managed and complete the Onboard playbook. Agents can use a server through AI Gateway after the server has been approved.

5.  [AI Gateway settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gateway.md)

    Confirm that AI Gateway is on, choose how tools are activated and deactivated, and activate the Data Sensitivity Check.

6.  [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md)

    Optional: Turn on client access control, and then create client access policies and turn on access management, so that each client is authorized to use only specific tools on an MCP server through AI Gateway.


