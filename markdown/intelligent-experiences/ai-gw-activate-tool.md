---
title: Activate or deactivate a tool
description: Allow agents to call one MCP server tool through AI Gateway, or block every call to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-activate-tool.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [MCP tools, activate tool, deactivate tool]
breadcrumb: [Govern tools and data, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Activate or deactivate a tool

Allow agents to call one MCP server tool through AI Gateway, or block every call to it.

## Before you begin

AI Gateway and the server's connection must be on. While either is paused, tools can't be changed.

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Open the MCP server record: navigate to **Settings** &gt; **AI Gateway**, and on the **Overview** tab, select the server name, or in AI Control Tower, navigate to **Inventory** &gt; **Assets** &gt; **MCP servers** and select the server name.

2.  Select the **AI Gateway** tab, and then select the **Tools** sub-tab.

3.  Select **Refresh tools**.

    If the server's authorization has expired, select **Reauthorize** first.

4.  Review the tool's **Scan status** and **Threat category**.

5.  Turn the tool's **Active** toggle on or off, and then select **Activate** or **Deactivate** in the confirmation dialog.


## Result

AI Gateway is set up to block every call to a tool when it's inactive. When a tool is active, agents can call it, and any policies for the tool apply to each call. The tool's status also shows in the **Available MCP tools** panel on the record's **Details** tab.

## What to do next

If **Automatically deactivate vulnerable tools** is on, a later scan can change a tool's status. For details, see [AI Gateway Tools tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-tools-tab.md).

