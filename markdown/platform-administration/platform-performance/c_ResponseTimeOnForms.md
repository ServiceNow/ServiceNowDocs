---
title: Reviewing response time on forms
description: A response time indicator \(clock\) appears at the end of many forms and lists.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Reviewing response time on forms

A response time indicator \(clock\) appears at the end of many forms and lists.

This indicator provides the processing time for a completed transaction, including the total time and the time for each step. Select the icon to show and hide the response time details. Hover over the icon to see a tooltip with the details. The following example shows the response time for retrieving a filtered list in a demo instance.

![Response time (ms): 3326, network: 75, server: 1963, browser: 1288](../image/ResponseTime2.png "Response time")

In this example, the transaction took the following amount of processing time:

-   3326 milliseconds total time
-   75 milliseconds moving data across the network
-   1963 milliseconds on the server

    **Note:** Server time is calculated using the following formula:

    ```
    server time = (client response time - browser time - client network time)
    ```

-   1288 milliseconds in the browser, rendering the HTML and parsing and executing JavaScript

A response time indicator doesn’t appear for simple operations, such as paging or changing a list sort order. The response time indicator also doesn't appear for the first transaction in a session.

To view a detailed breakdown of the processing time on forms, select the response time indicator icon.

![Response statistics](../image/ResponseTime1.png "Response time details")

Administrators can disable the response time by setting the **glide.ui.response\_time** property to **false** in the System Properties \[sys\_properties\] table. In the navigation filter, enter `sys_properties.list` and search for **glide.ui.response\_time**.

## Reviewing response times from system logs

You can use the system logs to review a list of response times for different transactions. To view the log, navigating to **All** &gt; **System Logs** and select the relevant log type. When you review response times, look for the following issues.

1.  A period where all transactions took an unusually long time. For example, transactions that normally took 1 second took 15 seconds between 11:00 AM and 11:20 AM. This issue can indicate that an unusual load, such as a large report, ran on that app server during that time.
2.  A specific transaction which repeatedly took an unusually long time. For example, the list of closed incidents sorted by short description took 30 seconds each time it was displayed. This issue can indicate that a particular transaction put an unusual database load on the system, such as sorting 500,000 records on an unindexed field.

If you notice issues with form response times, see [Improving response times on forms](improving-response-time-forms.md).

## Client transaction timings

The Client Transaction Timings plugin provides extra information about the time spent on both the client and server sides, by the browser and the network. This feature not only helps find long-running processes, but also provides information about where in the process the performance issue is caused.

For more information, see [Client transaction timings](../../time/reference/r_ClientTransactionTimings.md).

**Parent Topic:**[Monitoring platform performance](monitoring-platform-performance.md)

