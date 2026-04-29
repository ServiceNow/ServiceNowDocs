---
title: Log sources
description: Log Export Service \(LES\) can export log sources from some System Log Tables, the Audit Table, and Application Node Log Files.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
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

**Parent Topic:**[Exploring Log Export Service \(LES\)](les-landing-page.md)

