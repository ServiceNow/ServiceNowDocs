---
title: Edit a client access policy
description: Change the name, description, or tools of a client access policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-edit-client-access-policy.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [client access policy, edit policy, access management]
breadcrumb: [Control client access, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Edit a client access policy

Change the name, description, or tools of a client access policy.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  In AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers** and select the server name.

2.  Select the **AI Gateway** tab, and then select the **Policies** sub-tab.

3.  Under **Policy categories**, select **Access management**.

4.  In the **Client access** list, select the policy name, or select **Edit** from the actions menu on the policy's row.

    If a policy grants more tools than the page can load at once, a message explains that the policy can't be edited from this page.

5.  Change the **Policy name**, **Description**, or **Tools**.

    You can't change the client of an existing policy. To give a different client access, create a policy for that client. For details, see [Create a client access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-create-client-access-policy.md).

6.  Select **Save and close**.

    **Save and close** is available only after you change something.

    If someone else changed the policy after you opened it, your changes aren't saved. Close the panel and open the policy again to see its current state.


## Result

The changes appear in the **Client access** list.

**Important:** If access management is on for the server, it can take up to 30 minutes for the changes to apply to the client if it's already connected. For details, see [Controlling which tools clients can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-controlling-client-access.md).

