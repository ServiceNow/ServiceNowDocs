---
title: Define security controls for MCP Servers
description: Define security controls for an MCP Servers to determine which users can access it and what permissions they have.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/define-sec-mcp.html
release: australia
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Adding an MCP Server Console in AI Agent Studio, Configuring Model Context Protocol Client, MCP Client, AI Agent Studio, Enable AI experiences]
---

# Define security controls for MCP Servers

Define security controls for an MCP Servers to determine which users can access it and what permissions they have.

## Before you begin

Role required: sn\_mcp\_client.admin

## Procedure

1.  Open a Model Context Protocol Server and navigate to Access rules.

    You can select which users can access this MCP server via ACLs. The access control list \(ACL\) is generated after you define which category of users or specific user roles can access this MCP server. \[Omitted image "mcp-access-rules.png"\] Alt text: Define security controls for MCP Server.

2.  Select the users from the **Allowed users** drop down.

    There are three possible options for ACLs created in AI Agent Studio:

    -   **Any authenticated user**: Grants access to any user who is authenticated on the instance, regardless of the role.
    -   **Users with specified roles**: The default ACL option that requires you to select the specific roles required to invoke an AI agent or an agentic workflow. If you select this option, you will be able to add roles in the **Roles** field.

        **Note:** As the ACLs are Allow If ACLs, any user with at least one of the roles will be able to define specific roles that the users must have to discover and interact with this AI agent.

    -   **Public**: Grants access to all users, including guests who aren’t signed in.

        **Note:** Understand that this configuration should be used sparingly and only when needed.

3.  Select **Save**.


