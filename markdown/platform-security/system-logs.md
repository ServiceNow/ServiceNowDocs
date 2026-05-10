---
title: System logs
description: The System Logs module provides a variety of logs that you can use to troubleshoot and debug transactions and events that take place within the instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Logs, Platform Security]
---

# System logs

The System Logs module provides a variety of logs that you can use to troubleshoot and debug transactions and events that take place within the instance.

Access the following logs from the System Logs module:

|Log|Description|
|---|-----------|
|[Transactions](../../time/reference/r_TransactionLogs.md)|All application activity for an instance.|
|[Email](../../time/reference/r_EmailLogs.md) and [Push](../../time/reference/push-log.md)|All email notifications and Push messages sent from all instances within the system.|
|[Event Logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-events/event-logs-2.md)|All system events that occur within the system.|
|[Import](../../time/reference/r_ImportLogs.md)|Data import activity within the platform.|
|Table Changes|Changes made to all tables in the system.|
|[Outbound web services logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/outbound-request-logging.md)|All outbound web services requests such as REST and SOAP requests.|
|[System](../../time/reference/r_SystemLogs.md)|Warnings and errors for instance processes, records, and non-critical events, such as memory usage on the server machine.|

Use the [Log File Browser](../../time/reference/r_LogUtilities.md) to search and download logs. You can also search archived logs in the [log history](../../time/reference/r_LogHistory.md).

## Other logs

Your instance offers other logs in addition to those in the System Logs module. For example, the [System Diagnostics module](../../time/concept/c_SystemDiagnosticsApplication.md) provides upgrade history and slow query logs, which you can use to gain insight into how queries are affecting platform performance. The [Customer Updates table](../../time/reference/r_CustomerUpdatesTable.md) records every change that is made in the system.

