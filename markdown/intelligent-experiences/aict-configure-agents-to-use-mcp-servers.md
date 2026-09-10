---
title: Configure agents to use MCP servers
description: After client registration is complete, configure your AI agents to connect to MCP servers through AI Gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-configure-agents-to-use-mcp-servers.html
release: australia
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Configure agents to use MCP servers

After client registration is complete, configure your AI agents to connect to MCP servers through AI Gateway.

This configuration confirms all agent traffic is governed, secured, and observable. The configuration approach depends on how the MCP server was registered:

-   Register via AI Agent Studio: Update the existing agent to route through AI Gateway.
-   Register via AI Control Tower: Register the server in AI Agent Studio and then add it as a tool.
-   External agent platforms: For agents created on external platforms such as Microsoft Copilot Studio, Google Gemini, Amazon Bedrock, and others, set AI Gateway as the MCP Server endpoint.

