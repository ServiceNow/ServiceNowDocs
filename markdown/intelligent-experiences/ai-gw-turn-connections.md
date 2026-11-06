---
title: Turn AI Gateway connections on or off
description: Stop traffic through AI Gateway, for all MCP servers or for one server, while you investigate an issue, and turn it back on when you're done.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-turn-connections.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [AI Gateway, turn off AI Gateway, MCP server connections]
breadcrumb: [AI Gateway settings, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Turn AI Gateway connections on or off

Stop traffic through AI Gateway, for all MCP servers or for one server, while you investigate an issue, and turn it back on when you're done.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or admin

## Procedure

1.  In AI Control Tower, navigate to **Settings** &gt; **AI Gateway**.

2.  On the **Overview** tab, turn connections on or off.

    1.  For all MCP servers, use the toggle in the AI Gateway status banner.

    2.  For one MCP server, use the server's toggle in the **Connected** column.

3.  In the confirmation dialog, select **Pause** or **Resume**.


## Result

When you pause AI Gateway, the banner reads **AI Gateway is off**, and agents can't call any MCP server through it. When you pause one server, the change applies to every variant of that MCP server, and other servers continue to run. A variant is one of the connections registered for the same MCP server URL, for example by different users or with different credentials. Changes can take a few minutes to apply. When you resume AI Gateway, each server keeps its own connection status. You don't need to change any agent's configuration.

