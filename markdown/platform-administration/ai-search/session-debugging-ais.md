---
title: Enable session debugging for AI Search
description: Capture and review detailed AI Search log messages for a user session.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Search logging and debugging, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable session debugging for AI Search

Capture and review detailed AI Search log messages for a user session.

## Before you begin

Role required: admin

## About this task

When you enable session debugging for AI Search in a user session, the system records debug log messages for that session. These messages include:

-   Messages illustrating how AI Search interprets a user's search query
-   Messages specifying the search source filters and content security filters applied to a search query
-   Messages containing search query request and response objects in human-readable format

You can review these debug log messages to diagnose search issues or configure optimal search performance settings.

Once enabled, session debugging remains active for the user session until you disable it. For more information on session debugging, see Session debug.

## Procedure

1.  To enable debugging, navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug AI Search**.

    A message reports completion of the Debug AI Search session debug script.

2.  To review debug logs, navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Debug Log**.

    Debug log messages appear in the **Session Log** window.

3.  To disable debugging, navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug** &gt; **Disable All**.

    A message reports completion of the Disable All session debug script.


**Parent Topic:**[AI Search logging and debugging](../concept/logging-debugging-ais.md)

