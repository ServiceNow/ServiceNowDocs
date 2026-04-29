---
title: Transaction details
description: The Script Debugger displays transaction details for the current paused user session.The Script Debugger provides a standard set of transaction details for developers to debug and troubleshoot scripts.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Script Debugger user interface, Script Debugger, Debugging scripts, Scripting, API implementation, API implementation and reference]
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

**Parent Topic:**[Script Debugger user interface](../reference/parts-script-debugger-interface.md)

**Related topics**  


[Available transaction details](transaction-details.md#)

## Available transaction details

The Script Debugger provides a standard set of transaction details for developers to debug and troubleshoot scripts.

|Transaction element|Description|
|-------------------|-----------|
|**url**|The URL of the currently paused transaction.|
|**Request parameters**|The list of request parameters for this transaction. Each transaction has its own list of request parameters, but record transactions typically include the field values used to insert, update, or delete a record.|
|**instance**|The instance name.|
|**address**|The IP address of the end-user client system.|
|**session**|The user session ID.|
|**forward**|The IP address of the load balancer.|
|**query count**|The number of database queries the Script Debugger has made.|
|**thread**|The name of the thread running the Script Debugger instance.|
|**transactionid**|The Sys ID of the current transaction.|
|**token**|The Script Debugger token of the currently paused transaction. The system uses this token to identify different Script Debugger instances.|
|**name**|The name of the currently paused transaction. You can use this name to identify transactions in the logs.|
|**processor**|The name of the processor processing the current transaction, if present.|
|**method**|The HTTP request method the currently paused transaction uses.|
|**startTime**|The date-time stamp when the Script Debugger instance started.|
|**page**|The current table or UI page associated with the transaction.|
|**user**|The user who triggered the debug transaction.|
|**nodeid**|The Sys ID of the node running the Script Debugger instance.|

**Related topics**  


[Transaction details](transaction-details.md#)

