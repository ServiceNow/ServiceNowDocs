---
title: AI Gateway Policies tab
description: Use the Policies tab of the AI Gateway settings page to activate the Data Sensitivity Check, which helps filter personally identifiable information in MCP traffic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-policies-tab.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [AI Gateway, Data Sensitivity Check, sensitive data]
breadcrumb: [Explore, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI Gateway Policies tab

Use the Policies tab of the AI Gateway settings page to activate the Data Sensitivity Check, which helps filter personally identifiable information in MCP traffic.

When you select the **Policies** tab, the page heading changes to **Data Sensitivity Check**, the policy that the tab manages.

## Policy status

The banner shows whether the policy is activated. It reads **This policy is activated** or **This policy is deactivated**. Use the banner's toggle to activate or deactivate the policy for all servers, and then confirm with **Activate** or **Deactivate**. The change can take a few minutes to apply. While AI Gateway is paused, the toggle is unavailable. To define which data the policy detects, select **Configure sensitive data types**, which opens the Data Privacy configuration in a new browser tab.

## Servers running under this policy

The list shows each MCP server that the policy can apply to.

|Column|Description|
|------|-----------|
|Server name|The name of the MCP server. Select it to open a panel that lists the server's tools, where you can activate or deactivate the policy for each tool.|
|Active|A toggle that activates or deactivates the policy for this server, after you confirm. It's unavailable until the policy is activated for all servers, and while AI Gateway or the server's connection is paused.|

Use the **Search**, **Filter**, and **Refresh** icons above the list to find servers, filter them by policy status, and update the list.

To activate the policy and choose its servers, see [Activate the Data Sensitivity Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-activate-dsc.md).

## How the policy levels combine

The policy applies to a tool only when it's active at every level and connections aren't paused:

1.  For all servers, in the banner on this tab.
2.  For the server, in the **Active** column on this tab.
3.  For the tool. A tool follows the server's setting until you change it, which you can do in either of these places:

    -   On this tab: in the **Servers running under this policy** list, select the server name. A panel opens that lists the server's tools, each with its own **Active** toggle.
    -   On the MCP server record: in AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers**, select the server name, select the **AI Gateway** tab, and then select the **Policies** sub-tab.
    For details, see [Apply the Data Sensitivity Check to a server's tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-apply-dsc-tools.md).


