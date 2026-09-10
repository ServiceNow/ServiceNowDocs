---
title: Creating tools for a Model Context Protocol server
description: You can create tools from various tool categories to expose ServiceNow capabilities to Model Context Protocol \(MCP\) clients from MCP servers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/creating-tools-mcp-server.html
release: zurich
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 6
keywords: [Create tool for MCP server]
breadcrumb: [Configure, MCP Server Console, Enable AI experiences]
---

# Creating tools for a Model Context Protocol server

You can create tools from various tool categories to expose ServiceNow capabilities to Model Context Protocol \(MCP\) clients from MCP servers.

## MCP tools overview

Tools define which functionality and data an MCP server exposes to clients and the actions that can be performed on an instance by MCP clients. You can create tools based on the following capabilities:

-   [Subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-subflow-tool.md)
-   [Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-action-tool.md)
-   [Knowledge Graph schemas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-knowledge-graphs.md)
-   [REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-rest-api.md)
-   [AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-naskill.md), including custom skills created with AI Skill Kit

Tools include inputs that correspond to the fields of the existing capability. Any inputs that are enabled for a tool are exposed to clients. Each server must include at least one tool, and tools must be in the same application scope as any servers that contain them.

When clients receive a list of available tools from a server, they rely on tool descriptions to decide whether to call a tool and how to call it. Every tool description should answer two questions: what does this tool do and when should it be called. When creating tools, particularly REST API tools, make sure the description is clear and complete, otherwise clients may select the wrong tool for the job.

**Note:** A tool can be used by multiple servers. Changes that you make to a tool's name, description, or enabled inputs apply to any servers that use the tool. Before editing a tool, review which servers it's associated with to determine the impact for every server.

## MCP tools access

Existing access control lists \(ACLs\), role-based permissions, and field-level security all apply to tool calls made through an MCP server. MCP servers and tools don't bypass any ServiceNow access controls applied to the capabilities that tools are based on.

Evaluating ACL enforcement depends on who is calling a tool and which capability the tool is based on. If a caller lacks permission, tools can return an empty or incomplete result rather than an explicit authorization error so it's important to understand which type of enforcement applies to a given caller and tool type when troubleshooting unexpected results. MCP tool calls execute under one of two identities, which are evaluated differently:

-   **Human users**

    Tool calls execute under the authenticated user's own ServiceNow user identity. A user who can't read incident records in the platform can't retrieve them through an MCP tool either. All four layers of the standard access model apply: role-based access, contextual script-based ACLs, row- and field-level security, and deny-unless-permitted defaults.

-   **Autonomous agents**

    Tool calls execute under the identity of the integration user account rather than any individual end user's identity. What an agent can access is controlled by the integration user's roles and by the tool-level ACLs two layers, which are evaluated independently and both must permit the call for a tool to return data:

    -   The integration user must hold the roles required for every tool the agent will call. Under-provisioning this account causes tool calls to fail while over-provisioning creates unnecessary risk. For more information about configuring this account, see [Create an OAuth inbound integration for an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-oauth-inbound-integration-mcp-client.md).
    -   Tool-level ACLs control whether execution is permitted at the level of the tool itself, independent of the integration user's roles. Configuration requirements differ by tool type.

## ACL requirements for MCP tools

The configuration required for tool-level enforcement depends on which capability the tool is built from.

<table id="table_acl_by_tool_type"><thead><tr><th>

Tool type

</th><th>

ACL configuration

</th></tr></thead><tbody><tr><td>

AI skill tools

</td><td>

An execute ACL and role masking is required for any custom AI skill to be used as a tool. Otherwise a tool can return empty results instead of an authorization error, which can be difficult to diagnose as a permissions issue rather than a data issue.For more information, see [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/create-new-skill.md) and [Create a tool from an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-naskill.md).

</td></tr><tr><td>

Subflow and Action tools

</td><td>

An AI ACL is required for any Subflow or Action to be used as an MCP tool.For more information, see [Create an AI ACL for a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-acl.md) and [Check the compatibility of a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/check-compatibility-of-subflow.md).

</td></tr><tr><td>

Knowledge Graph tools

</td><td>

ACL enforcement happens at the node level during every graph traversal. Two users or agents with different permissions issuing the identical query can receive different results, based on what each caller is permitted to see.For more information, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md) and [Create a tool from a Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-knowledge-graphs.md).

</td></tr></tbody>
</table>-   **[Create a tool from a Subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-subflow-tool.md)**  
Create a tool from a Subflow to expose it to Model Context \(MCP\) clients from an MCP Server.
-   **[Create a tool from an Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-action-tool.md)**  
Create a tool from an Action to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.
-   **[Create a tool from a Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-knowledge-graphs.md)**  
Create a tool from a Knowledge Graph to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.
-   **[Create a tool from a REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-rest-api.md)**  
Create a tool from a REST API to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.
-   **[Create a tool from an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-a-tool-from-naskill.md)**  
Create a tool from a generative AI skill to expose it to Model Context Protocol \(MCP\) clients from an MCP Server.

**Parent Topic:**[Configuring MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configuring-mcp-server-console.md)

**Related topics**  


[Create an AI ACL for a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-acl.md)

[Check the compatibility of a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/check-compatibility-of-subflow.md)

[Create an OAuth inbound integration for an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-oauth-inbound-integration-mcp-client.md)

