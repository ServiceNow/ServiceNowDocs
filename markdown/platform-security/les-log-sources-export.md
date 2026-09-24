---
title: Log sources
description: Log Export Service \(LES\) can export log sources from some System Log Tables, Audit Tables, and Application Node Log Files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/les-log-sources-export.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Log Export Service \(LES\), Platform Security]
---

# Log sources

Log Export Service \(LES\) can export log sources from some System Log Tables, Audit Tables, and Application Node Log Files.

LES can export the following log sources:

-   System Log Tables
    -   **syslog**: Warnings and errors for instance processes, records, and non-critical events such as memory usage
    -   **syslog\_transaction**: View all browser activity for an instance
    -   **sys\_outbound\_http\_log**: View all requests and responses for outbound web services such as REST and SOAP
-   Audit tables
    -   **sys\_audit**: Record changes made to tables chosen to be audited
    -   **sys\_audit\_delete**: Snapshots produced when audited records are deleted
    -   **sys\_audit\_relation**: Changes to tracked reference fields on audited records
-   Workflow/Process logs: **sys\_flow\_log** records execution details and status of workflow processes
-   Security and authentication logs: **sys\_user\_login\_history** tracks user login attempts and authentication events
-   Application node log files: Use the localhost log files to view application node errors. Your instance has multiple nodes and each node has multiple log files.

These log sources provide comprehensive visibility into system operations, user activity, and integration points. Export these logs to external systems for long-term retention, compliance auditing, or security analysis.

For detailed schema information and purposes for each log source, see [System logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/system-logs.md).

**Parent Topic:**[Exploring Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-landing-page.md)

