---
title: Available transaction details
description: The Script Debugger provides a standard set of transaction details for developers to debug and troubleshoot scripts.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Script Debugger and Session Log, Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Available transaction details

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

**Parent Topic:**[Script Debugger and Session Log](../concept/script-debugger.md)

**Related topics**  


[Transaction details](https://www.servicenow.com/docs/access?context=transaction-details&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

