---
title: Controlling which tools clients can access
description: Limit each client to the MCP server tools that it requires by turning on access management for the server and creating client access policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-controlling-client-access.html
release: australia
topic_type: concept
last_updated: "2026-10-26"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, access management, client access policy, MCP tools, AI Gateway]
breadcrumb: [Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Controlling which tools clients can access

Limit each client to the MCP server tools that it requires by turning on access management for the server and creating client access policies.

## Client based access control

By default, clients registered for an MCP server can call any active tool on that server. Because the MCP server receives requests from AI Gateway rather than from the clients behind it, the MCP server can't tell which client sent a request. AI Gateway is the last point in the connection that can identify which client sent a request, so it's where you control which tools each client can use.

Client access control works at two levels:

1.  For the instance, a user with the aig\_admin role turns on client access control with a system property. Until then, access management isn't available for any MCP server.
2.  For each MCP server, an AI steward turns on access management on the server's record and creates client access policies. Each policy grants one client access to specific tools on that server.

When access management is on for a server, a client is authorized to use only the tools that its client access policies grant through AI Gateway. A client that has no policy on the server isn't authorized to use any of the server's tools through AI Gateway. A client is authorized to use every tool that any of its policies grants, whether it has one policy or several. When access management is off, every client can use all of the server's active tools.

Client access policies work alongside tool status. When a tool is inactive, AI Gateway is set up to block calls to it, even from a client that a policy grants the tool to. For details, see [Activate or deactivate a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-activate-tool.md).

Before you create policies, register the clients for the server. For details, see [Connecting agents through AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-connecting-agents.md).

-   [Turn on client access control for your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-on-client-access.md): let AI stewards use access management on this instance.
-   [Create a client access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-create-client-access-policy.md): grant a client access to specific tools.
-   [Turn access management on or off for an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-access-management.md): start or stop enforcing client access policies for one MCP server.
-   [Edit a client access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-edit-client-access-policy.md): change a policy's name, description, or tools.
-   [Delete a client access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-delete-client-access-policy.md): remove the access that a policy grants.

## Client access enforcement

A client authenticates with your instance and receives an access token, which it uses for its requests to AI Gateway. The first time AI Gateway receives a request with a new token, it exchanges the token with your instance. Along with the token for the MCP server, your instance returns the list of tools that the client is allowed to use. AI Gateway is designed to show the client only those tools and deny any request for another tool.

## When changes take effect

AI Gateway gets a client's allowed tools when it exchanges the client's access token. A client that's already connected keeps the tools from its current token until the token is renewed. Access tokens are valid for 30 minutes by default.

**Important:** When you create, edit, or delete a client access policy, or turn access management on or off, it can take up to 30 minutes for the change to apply to clients that are already connected.

## Where you manage client access

You manage client access on the MCP server record. In AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers**, select the server name, select the **AI Gateway** tab, and then select the **Policies** sub-tab. When client access control is on for the instance, the **Policy categories** list starts with **Access management**, which opens by default. Its count is the number of client access policies on the server.

The **Access management** card shows whether access management is on for the server and has a toggle switch to turn it on or off. Below the card, the **Client access** list shows the server's client access policies.

|Column|Description|
|------|-----------|
|Policy name|The name of the policy. Select it to edit the policy.|
|Client|The client that the policy grants access to.|
|Target|The tools that the client is authorized to use under this policy.|
|Updated|When the policy was last changed.|

Each row's actions menu has **Edit** and **Delete**. Use the **Search** and **Filter** icons above the list to find policies by keyword or by when they were last updated.

