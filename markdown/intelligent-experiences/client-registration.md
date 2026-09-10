---
title: Client registration and AI Gateway setup
description: Once an MCP server has been managed and approved, register the clients that will connect to it via AI Gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/client-registration.html
release: australia
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 1
breadcrumb: [Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Client registration and AI Gateway setup

Once an MCP server has been managed and approved, register the clients that will connect to it via AI Gateway.

Client registration establishes a secure OAuth 2.1 connection between your AI agent platform and the MCP server through AI Gateway. The registration process generates credentials — client ID and client secret to authenticate your agents when they make requests to the MCP server.

## Selecting a registration type

When you add a client to an MCP server, you can choose between two registration types:

-   **CIMD client:** Automated registration with a Client Identity Meta-data Document. The client’s metadata URL is checked, and OAuth credentials are created automatically. Currently supported for VS Code only.
-   **MCP client:** Manual registration. You enter a client name and a redirect URL. Use this for AI Agent Studio, Postman, Claude Desktop, Copilot Studio, and all other platforms.

