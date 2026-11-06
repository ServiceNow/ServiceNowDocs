---
title: AI Gateway Tools tab
description: Use the Tools tab of the AI Gateway settings page to choose whether tools are automatically deactivated after a security scan or activated after approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-tools-tab.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [AI Gateway, MCP tools, vulnerable tools]
breadcrumb: [Explore, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI Gateway Tools tab

Use the Tools tab of the AI Gateway settings page to choose whether tools are automatically deactivated after a security scan or activated after approval.

AI Gateway scans each tool that it fetches from an MCP server. The settings on this tab decide what happens next.

|Setting|What it does|
|-------|------------|
|Automatically deactivate vulnerable tools|When it's on, tools that the scan finds vulnerable are deactivated automatically, including tools that are in use, which also affects active client calls to them. If a later scan finds that the vulnerability has been removed, the tools are activated again. When it's off, vulnerable tools aren't deactivated automatically.|
|Automatically activate new tools|When it's on, tools that AI Gateway fetches after an MCP server has been approved are activated automatically. When it's off, newly fetched tools aren't activated automatically.|

To change a setting, use its toggle, and then select **Turn on** or **Turn off** in the confirmation dialog. The settings apply to all MCP servers connected through AI Gateway. To activate or deactivate one tool on one server, see [Activate or deactivate a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-activate-tool.md).

