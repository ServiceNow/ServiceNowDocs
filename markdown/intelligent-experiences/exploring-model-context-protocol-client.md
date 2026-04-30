---
title: Explore Model Context Protocol Client
description: The Model Context Protocol \(MCP\) client in ServiceNow is a framework that allows AI agents, such as large language models \(LLMs\), to interact with and manage ServiceNow instances. This interaction takes place within a server-client architecture.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-02"
reading_time_minutes: 1
breadcrumb: [Model Context Protocol Client, Now Assist AI agents, Enable AI experiences]
---

# Explore Model Context Protocol Client

The Model Context Protocol \(MCP\) client in ServiceNow is a framework that allows AI agents, such as large language models \(LLMs\), to interact with and manage ServiceNow instances. This interaction takes place within a server-client architecture.

## Model Context Protocol Client terminology

-   **MCP host**

    The AI application environment where the tasks are initiated.

-   **MCP client**

    Manages communication between the host and the MCP servers, handling the requests and responses.

    The MCP Client architecture enables AI agents to extend their capabilities by invoking external systems dynamically, which enables tasks like accessing APIs, databases, or file systems in a standardized way.

-   **MCP server**

    Provides external functionalities by exposing tools for AI agents to use.

-   **MCP tools**

    The external tools exposed by the MCP servers to be used by AI agents.


## Why use MCP tools

MCP tools enable seamless integration to:

-   Connect your AI agent with a wide variety of external tools with minimal setup.
-   Add multiple MCP tools to an AI agent to perform a broader range of tasks.
-   Review and edit tool input parameters as needed before saving.

