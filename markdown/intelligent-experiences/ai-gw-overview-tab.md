---
title: AI Gateway Overview tab
description: Use the Overview tab of the AI Gateway settings page to turn connections through AI Gateway on or off, for all MCP servers or for one server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-overview-tab.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [AI Gateway, MCP server connections]
breadcrumb: [Explore, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# AI Gateway Overview tab

Use the Overview tab of the AI Gateway settings page to turn connections through AI Gateway on or off, for all MCP servers or for one server.

## AI Gateway status

The banner at the top of the tab shows whether AI Gateway is on. When it's on, the banner reads **AI Gateway is on** and notes that you can still control individual MCP server connections independently. When it's off, the banner reads **AI Gateway is off**. Use the banner's toggle to pause or resume all connections through AI Gateway. You're asked to confirm, and the change can take a few minutes to apply. When you resume connections, each server keeps its own connection status.

## MCP servers list

The **MCP servers** list shows each MCP server that connects through AI Gateway, with the number of servers next to the heading. Use it to turn traffic to individual servers off or on, independently of each other. While AI Gateway is off, all **Connected** toggles are off and can't be changed.

|Column|Description|
|------|-----------|
|Server name|The name of the MCP server. Select it to open the server's record on its **AI Gateway** tab. To come back, select **AI Gateway \(Overview\)** at the top of the record.|
|Last updated|The date and time when the server's connection setting last changed.|
|Last updated by|The user who last changed the server's connection setting.|
|Connected|A toggle that pauses or resumes this server's connections through AI Gateway, after you confirm. The change applies to every variant of this MCP server, and other servers aren't affected. A variant is one of the connections registered for the same MCP server URL, for example by different users or with different credentials.|

Use the **Search**, **Filter**, and **Personalize columns** icons above the list to find servers, filter them by connection status or last update, and choose which columns to show. The **Connected** column is always shown.

To turn connections on or off, see [Turn AI Gateway connections on or off](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-turn-connections.md).

