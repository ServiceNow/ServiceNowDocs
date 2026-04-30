---
title: JavaScript API Context-sensitive help
description: The syntax editor can display context-sensitive API information.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# JavaScript API Context-sensitive help

The syntax editor can display context-sensitive API information.

JavaScript API Context-sensitive help includes the ability to:

-   List script elements that are valid at the cursor's location. The system displays suggestions in a pop-up window.
-   Add a selected script element at the cursor's location. If the cursor is within or adjacent to a partial entry, the system completes the entry with the selected script element.
-   View API documentation for a selected suggestion.
-   View the expected parameters and format of the current script element.

If the cursor is adjacent to a text string, the system searches for script elements that start with this text string. For example, while the cursor is within or adjacent to the string `GlideR`, the system displays script elements such as:

-   GlideRecord
-   GlideRecordSecure

Context-sensitive suggestions are based on script type. For example, when working on a business rule, only suggestions from the server API and for objects such as **current** and **previous** display. When working on a client script, the system only displays suggestions from the client API.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

