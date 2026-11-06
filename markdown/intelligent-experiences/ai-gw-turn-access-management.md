---
title: Turn access management on or off for an MCP server
description: Turn on access management to limit each client to the tools that its policies grant, or turn it off to let every client use all active tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-turn-access-management.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [access management, client access policy, MCP server]
breadcrumb: [Control client access, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Turn access management on or off for an MCP server

Turn on access management to limit each client to the tools that its policies grant, or turn it off to let every client use all active tools.

## Before you begin

-   Client access control must be turned on for the instance. For details, see [Turn on client access control for your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-on-client-access.md).
-   The MCP server must be approved. For details, see [MCP server approval playbook workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-mcp-server-approval-playbook-workflow.md).
-   Client access policies should be created for the clients that use the server. After access management is on, clients without a policy aren't authorized to use the server's tools through AI Gateway. For details, see [Create a client access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-create-client-access-policy.md).

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  In AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers** and select the server name.

2.  Select the **AI Gateway** tab, and then select the **Policies** sub-tab.

3.  Under **Policy categories**, select **Access management**.

4.  On the **Access management** card, turn the toggle switch on or off.

5.  In the confirmation dialog, select **Turn on** or **Turn off**.

    To leave the setting as it is, select **Keep off** or **Keep on**.


## Result

The card shows **Access management is on** or **Access management is off**.

-   When access management is on, only the clients that the server's client access policies allow are authorized to access the server through AI Gateway, and each client is authorized to use only the tools that its policies grant.
-   When access management is off, every client can access the server and use all of its active tools. The server's client access policies aren't deleted, but AI Gateway doesn't apply them until access management is turned on again.

**Important:** It can take up to 30 minutes for the change to apply to clients that are already connected. For details, see [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md).

