---
title: Debugging remote table script definitions
description: You can enable session debugging for remote table script definitions. To enable script definition logging in a session debug log, set the glide.script.vtable.log.debug property to true.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Debugging remote table script definitions

You can enable session debugging for remote table script definitions. To enable script definition logging in a session debug log, set the **glide.script.vtable.log.debug** property to **true**.

When you create remote table script definitions, you can use the `gs.debug()` command to add debug logs that are visible in the session debugger. The session debugger also contains debug logs with \[RemoteTable\] tags, each with the following information:

-   Query definition
-   Number of rows loaded in the remote table
-   Number of aggregate rows `(if GlideAggregate)`

Prolonged use of the **glide.script.vtable.log.debug** property can affect performance, so it is best to set its value to **false** when you finish a debugging session.

**Note:** If you are not on the application node that processed your remote table script, you may not see the resulting log statements. In this case, contact Technical Support.

Use the v\_query.setLastErrorMessage\(message\) API to set the last error message that appears at the bottom of the list view. In script, you can retrieve this message using the glideRecord.getLastErrorMessage\(\) API. To learn more about these APIs, see Text-To-Display.

**Parent Topic:**[Remote tables](../concept/remote-tables.md)

**Related topics**  


[bundle-platadm.r_AvailableSystemProperties]

[bundle-crapiref.script-debugger]

