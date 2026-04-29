---
title: Tables excluded from rollback after running an automated test
description: The Automated Test Framework tracks data created by running tests and rolls back changes after testing. The system excludes certain tables from being tracked during testing.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Tables excluded from rollback after running an automated test

The Automated Test Framework tracks data created by running tests and rolls back changes after testing. The system excludes certain tables from being tracked during testing.

The system excludes certain tables from being tracked or rolled back:

-   The [History \[sys\_history\_line\] table](https://www.servicenow.com/docs/access?context=c_HistorySets&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   The [ECC Queue table \[ecc\_queue\]](https://www.servicenow.com/docs/access?context=r_DiscoveryStatusECCQueue&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   The Email [\[sys\_email\]](https://www.servicenow.com/docs/access?context=c_SystemMailboxes&version=australia&pubname=australia-platform-administration&ft:locale=en-US) [Email Log \[sys\_email\_log\]](https://www.servicenow.com/docs/access?context=r_EmailLogs&version=australia&pubname=australia-platform-security&ft:locale=en-US) tables
-   The [Report Executions \[report\_executions\] and ReportStats \[report\_stats\]](https://www.servicenow.com/docs/access?context=report-statistics&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) tables.
-   The Execution Tracker \[sys\_execution\_tracker\] tables
-   The Progress Worker \[sys\_progress\_worker\] table
-   The Schema Change \[sys\_schema\_change\]
-   The Upgrade History \[sys\_upgrade\_history\] and Upgrade History Log \[sys\_upgrade\_history\_log\] tables
-   The Mutex \[sys\_mutex\] table
-   The Plugin Log \[sys\_plugin\_log\] table
-   The Status \[sys\_status\] table
-   The Number Counter \[sys\_number\_counter\] table
-   The AMB Channel Presence \[sys\_amb\_channel\_presence\] table
-   Any table that extends an excluded table.
-   Any table starting with the following prefixes are also excluded:
    -   syslog
    -   sys\_amb\_message
    -   sys\_cluster
    -   cmdb\_metric
    -   ts\_
    -   v\_
    -   sys\_delete\_recovery

If your test run changes \(inserts/updates/deletes\) any record on these excluded tables, the system does not roll back the change after testing.

**Parent Topic:**[Automated Test Framework \(ATF\) reference](../concept/atf-ref-overview.md)

