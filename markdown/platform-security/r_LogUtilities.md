---
title: Use the log file browser
description: The instance provides the utilities log file browser and log file download.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# Use the log file browser

The instance provides the utilities log file browser and log file download.

Use **System Logs** &gt; **Utilities** &gt; **Node Log File Browser** to view any system log entry. You can search for log files by using the following filters:

|Field|Description|
|-----|-----------|
|Start time|Start date and time of the range you want to search, for the locale of the machine running the instance.|
|Session ID|System-generated hexadecimal string that identifies the session that generated the log entry.|
|End time|End date and time of the range you want to search, for the locale of the machine running the instance.|
|Message|System-generated description of the occurrence.|
|Level|Type of message displayed. The levels are Debug, Error, Warning, and Information. A warning is an error that has been handled and recovered. An error is something that must be fixed.|
|Thread name|System-generated identifier of the thread that created the log file.|
|Max rows|Maximum number of records returned for a particular filter.|

The instance creates compressed archives of system logs every 2 days and purges log archives after 21 days.

**Important:** When a node is retired, the node's log files are purged immediately, which means they aren't archived for an additional 21 days.

You can download log file archives and view them with **System Logs** &gt; **Utilities** &gt; **Node Log File Download**. Select a log archive from the list, and then click **Download log** under Related Links to open or save the archive.

**Note:** Log files are only available for the node you are currently logged into. To see the currently logged into node, navigate to **System Diagnostics** &gt; **Stats**.

Use the new **Show Syslog Records** button on the Transaction and Active Transaction forms to view any System Log entries that were generated during the execution of the transaction. A transaction can have any number of syslog entries. The multiple syslog entries for all the transactions make it difficult to co-relate a transaction with their respective syslog entries. The **Show Syslog Records** UI action helps in co-relating the active and completed transactions to their respective syslog entries by building a URL to query the syslog table. Identifying the correct syslog entries for a particular transaction helps in debugging and addressing security concerns.

