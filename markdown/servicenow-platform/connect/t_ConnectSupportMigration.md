---
title: Migrate from legacy chat to Connect Support
description: Connect Support is an extension of Connect. Users designated as support agents have access to the support tab of the connect sidebar. Do not use Connect Support concurrently with legacy chat.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect Support administration, Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Migrate from legacy chat to Connect Support

Connect Support is an extension of Connect. Users designated as support agents have access to the support tab of the connect sidebar. Do not use Connect Support concurrently with legacy chat.

## Before you begin

Role required: admin

Before you activate Connect Support, inform your support agents to close out any existing chats.

Legacy chat uses a different field to determine which state a help desk chat is in. A fix script is included in the Connect Support plugin that circumvents this issue by closing out any existing help desk chat sessions. Manually closing out any existing chats before allowing this script to run helps prevent any loss of chat information.

If you do not close out existing help desk chats, your metrics and chat queue will not work accurately.

## Procedure

1.  Activate the Connect Support plugin.

    When you activate the Connect Support plugin, the **glide.connect.support.enabled** property redirects the legacy chat URL to Connect Support.

    For more information, see [Activate Connect Support](t_ActivateConnectSupport.md#).

2.  Hide the Social IT application.

    Activating Connect Support does not completely eliminate the legacy chat module. To prevent users from using the legacy chat, hide the Social IT application menu. For more information, see Enable or disable an application menu or module .


