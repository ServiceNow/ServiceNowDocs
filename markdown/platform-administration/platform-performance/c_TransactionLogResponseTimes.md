---
title: Reviewing transaction logs
description: The instance automatically logs the vital statistics of every transaction that it processes, and that information is available to you as an administrator. Reviewing transaction logs can help identify latency and performance issues.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Monitor, Platform performance, Maintain and monitor, Administer]
---

# Reviewing transaction logs

The instance automatically logs the vital statistics of every transaction that it processes, and that information is available to you as an administrator. Reviewing transaction logs can help identify latency and performance issues.

To view the transaction log, log in to your instance and navigate to **All** &gt; **System Logs** &gt; **Transactions**.

To see the average response time of all listed transactions, select and hold \(or right-click\) the column **Response time**. Select **Configure** &gt; **List Calculations**, and then select the **Average value** check box.

You can limit the list to those transactions that took place during the time period of interest. The default filter returns transactions from today.

For each completed transaction, available information includes the following \(times are in milliseconds\):

-   Date/time, User ID, IP address, and URL of the transaction.
-   Total response time, which doesn’t include the browser time because the server doesn’t have that information.
-   **Output length**: how many bytes the transaction returned, after any compression.
-   **SQL time**: time spent executing SQL commands.
-   **SQL count**: number of SQL commands executed.
-   **Business rule time**: time spent processing business rules.
-   **Business rule count**: number of business rules executed.
-   **Network time**: network transmission time, both from and to the user.

**Note:** You can change which columns are shown and their order by selecting the Update Personalized List icon \(![](../../../common/image/gear.png)\)

**Parent Topic:**[Monitoring platform performance](monitoring-platform-performance.md)

