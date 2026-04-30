---
title: Log sources
description: Log Export Service \(LES\) can export log sources from some System Log Tables, the Audit Table, and Application Node Log Files.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Log Export Service \(LES\), Platform Security]
---

# Log sources

Log Export Service \(LES\) can export log sources from some System Log Tables, the Audit Table, and Application Node Log Files.

The following are the log sources that can be exported by LES.

-   System Log Tables
    -   syslog table: View warnings and errors for instance processes, records, and non-critical events, such as memory usage on the server machine
    -   syslog\_transaction table: view all browser activity for an instance
    -   sys\_outbound\_http\_log table: view all requests and responses for outbound web services such as REST and SOAP
-   Audit Table: Use the sys\_audit table view record changes made to tables chosen to be audited
-   Application Node Log Files: Use the localhost log files to view application node errors. Your instance will have multiple nodes and each node will have multiple log files.

See [System logs](../../system-logs/concept/system-logs.md) to learn more about the schema and purpose for the above log sources.

**Note:** LES forwards logs exclusively when they are generated through the logging framework. The following are the two sources for which logs are not getting forwarded:

|Source name|Reason|
|-----------|------|
|datacollector|Data is inserted directly into the syslog child table, which causes it to appear in the syslog table as well. However, this bypasses the logging framework, so the records reach the syslog table but are not forwarded to the topic.|
|com.glide.ui.ServletErrorListener|Logs are inserted into the syslog table using the NoBroadcast logging variant, where the broadcast flag is set to false. In this mode, logs are written to syslog but are not forwarded to external consumers because they do not pass through the logging framework.|

**Parent Topic:**[Exploring Log Export Service \(LES\)](les-landing-page.md)

