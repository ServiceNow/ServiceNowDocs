---
title: Transaction details
description: The Script Debugger displays transaction details for the current paused user session.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Transaction details

The Script Debugger displays transaction details for the current paused user session.

Transaction details are available in a dedicated resizeable section underneath the Call Stack on the bottom left of the Script Debugger.

![Transaction details](../image/sd_transaction_details.png "Example transaction details")

The Script Debugger only displays transaction details when it pauses on a script. Developers can use transaction details to:

-   Inspect the URL of the currently paused transaction.
-   Inspect the request parameters for the currently paused transaction.
-   Inspect network information about the current transaction.
-   Inspect the user and session ID that initiated the debug transaction.

**Parent Topic:**[Script Debugger and Session Log](script-debugger.md)

**Related topics**  


[Available transaction details](../reference/available-transaction-details.md)

