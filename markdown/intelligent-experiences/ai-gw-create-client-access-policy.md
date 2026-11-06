---
title: Create a client access policy
description: Grant one client access to specific tools on an MCP server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-create-client-access-policy.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 2
keywords: [client access policy, access management, MCP tools, MCP client]
breadcrumb: [Control client access, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a client access policy

Grant one client access to specific tools on an MCP server.

## Before you begin

-   Client access control must be turned on for the instance. For details, see [Turn on client access control for your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-on-client-access.md).
-   The client must be registered for the MCP server, or be a Client ID Metadata Document \(CIMD\) client. For details, see [Connecting agents through AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-connecting-agents.md).

Role required: sn\_ai\_governance.ai\_steward

## About this task

A policy grants access to one client. To grant several clients access, create a policy for each client. A client is authorized to use every tool that any of its policies grants, whether it has one policy or several.

## Procedure

1.  In AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers** and select the server name.

2.  Select the **AI Gateway** tab, and then select the **Policies** sub-tab.

3.  Under **Policy categories**, select **Access management**.

4.  In the **Client access** section, select **Create client access policy**.

    The **Server scope** field shows the current MCP server. A client access policy applies only to the server that it's created on.

5.  In the **Policy name** field, enter a name for the policy.

    The name must be unique on this MCP server, regardless of case, and can be up to 100 characters. It can't contain HTML tags.

6.  In the **Description** field, enter a description of up to 255 characters.

7.  In the **Client** list, select the client that receives access.

    The list shows the clients registered for this server and the CIMD clients on the instance. If the list shows `No clients available for this server`, register a client first.

8.  In the **Tools** field, search for and select each tool that the client can use, or select **Add all tools**.

    The selected tools appear below the field. To remove a tool, select the close icon on its label.

    **Add all tools** adds the tools that are on the server when you select it. Tools that the server exposes later aren't added to the policy.

    Inactive tools appear with **\(Inactive\)** after their names. You can add them, but AI Gateway is set up to block calls to them until they're activated.

9.  Select **Save and close**.

    **Save and close** is available after you enter a policy name, select a client, and add at least one tool.


## Result

The policy appears in the **Client access** list, and the count next to **Access management** increases.

**Important:** If access management is on for the server, it can take up to 30 minutes for the policy to apply to clients that are already connected. For details, see [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md).

## What to do next

If access management is off for the server, the policy isn't enforced until you turn it on. For details, see [Turn access management on or off for an MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-access-management.md).

