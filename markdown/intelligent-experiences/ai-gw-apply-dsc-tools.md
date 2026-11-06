---
title: Apply the Data Sensitivity Check to a server's tools
description: Choose which of an MCP server's tools the Data Sensitivity Check inspects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-apply-dsc-tools.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [Data Sensitivity Check, MCP tools]
breadcrumb: [Govern tools and data, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Apply the Data Sensitivity Check to a server's tools

Choose which of an MCP server's tools the Data Sensitivity Check inspects.

## Before you begin

The Data Sensitivity Check must be activated for all servers. For details, see [Activate the Data Sensitivity Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-activate-dsc.md).

AI Gateway and the server's connection must be on. While either is paused, the policy can't be changed.

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Open the MCP server record: navigate to **Settings** &gt; **AI Gateway**, and on the **Overview** tab, select the server name, or in AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers** and select the server name.

2.  Select the **AI Gateway** tab, and then select the **Policies** sub-tab.

3.  In the **Policy categories** list, select **Data sensitivity**.

4.  On the **Data sensitivity check** card, if the banner reads **This policy is deactivated**, select **Activate**, and then select **Activate** in the confirmation dialog.

5.  In the **Tools** list, select **Deactivate** for each tool that the policy shouldn't inspect, or **Activate** to include a tool again, and confirm each change in the dialog. The buttons are available only after the policy is activated for the server.


## Result

The tool's **Policy status** changes to Active or Inactive. The policy inspects a tool only when it's active for all servers, for the server, and for the tool, and connections aren't paused.

