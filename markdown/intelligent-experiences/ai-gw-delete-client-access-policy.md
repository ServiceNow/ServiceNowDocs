---
title: Delete a client access policy
description: Remove a client access policy and the access to tools that it grants a client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-delete-client-access-policy.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [client access policy, delete policy, access management]
breadcrumb: [Control client access, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Delete a client access policy

Remove a client access policy and the access to tools that it grants a client.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  In AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers** and select the server name.

2.  Select the **AI Gateway** tab, and then select the **Policies** sub-tab.

3.  Under **Policy categories**, select **Access management**.

4.  In the **Client access** list, select **Delete** from the actions menu on the policy's row.

5.  In the confirmation dialog, select **Delete**.

    You can't undo a deletion.


## Result

The policy is removed from the **Client access** list. If access management is on for the server, the client loses access to the tools that only this policy granted. If the client has no other policy on the server, it's no longer authorized to use any of the server's tools through AI Gateway.

**Important:** It can take up to 30 minutes for the deletion to apply to the client if it's already connected. Until then, the client can still use the tools that the policy granted. For details, see [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md).

