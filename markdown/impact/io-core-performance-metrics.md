---
title: Transaction or response metrics
description: The metrics provide a performance snapshot of classic UI transactions within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-core-performance-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 6
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Transaction or response metrics

The metrics provide a performance snapshot of classic UI transactions within the ServiceNow AI Platform®.

## User transaction count \(sum\)

Transaction count is the instance-wide sum of all UI transactions of a certain type known as **UI\_TYPE**, which is a classification used only in ServiceNow proprietary code.

**UI\_TYPE** excludes all AJAX, Angular, REST \(including all ServicePortal and /api/now/ui/\), Scheduler, Agent Workspace, SOAP etc. Essentially, it can be considered to cover only classic, whole page transaction types for example, table based form/list transactions excluding List V3, home pages, UI pages.

This is useful to understand core business hours. Potentially useful as a secondary identifier of extreme performance issues if the number rapidly changes in minutes and stays that way for at least 10 minutes either up or down.

**Note:** This indicator is only a secondary indicator, which can be used to understand the context where it is used, and cannot be directly used for troubleshooting.

## Average server response time \(weighted average\)

Server response time in this context is the average/mean execution time for **UI\_TYPE** transactions. See Transaction Count \(sum\) for limitations of this classification.

In addition to these limitations, Server Response time also does NOT include:

-   Time spent on waiting for a semaphore \(if all semaphores are used by other users\).
-   Time spent waiting for session sync \(if current user already has an active transaction\).
-   Time spent on the network back and forth to ServiceNow.
-   Time spent on the client-side by the browser or mobile device.

Server response time commonly fluctuates up and down in relation to core business hours due to the type of operations that tend to occur at any given time. Thus, it is very common that server response time appears more volatile during nights and weekends because administrators are running long reports or administrative transactions that typically take longer to execute. This, combined with the fact that fewer overall transactions are occurring, means a few slow transactions will have greater impact on the average.

When considering long-term trends, like Week over week comparisons for example, one should consider that such changes may simply reflect usage pattern changes, such as users doing more or less of certain types of transactions that are typically faster or slower. Because each transaction type has different functional requirements, there is no arbitrary threshold for what constitutes a **slow** transaction and thus no threshold should be applied to this metric. Instead of looking at long-term trends or short spikes outside core business hours, attention should be placed on extreme deviations from the norm or where this metric coincides with another performance indicator.

Since this metric is limited to the response time of **UI\_TYPE** transactions \(see definition under Transaction Count \(sum\)\), it may be a very incomplete picture of your end user's performance. Other methods of measuring should be considered for aspects of total system performance.

## Stacked time: Server response time, Network time \(network time, both from and to the user\) and browser time

Server, network, and browser response times are three key metrics in the life cycle of a transaction. Average Stacked time of a transaction provides an response time from three metrics in a pile of objects.

-   **Server Time**

    The number of milliseconds spent by the server in fulfilling the transaction. It does not include:

    -   server time spent prior to a redirect \(HTTP 302\)
    -   time spent on subsequent, partial page requests \(that is, AJAX\) or serving up a resource \(CSS, JavaScript, images, etc\)
    -   wait time from waiting for a semaphore or waiting for a previous transaction on the same session to complete
    Therefore, this can be a confusing and inflated metric because some transactions may have 90% or more of their response time spent waiting for another transaction to complete.

-   **Network Time**

    It is the time it takes the server to write all the bytes of the request to the output stream - not the time it takes to transmit those bytes across the internet. This is not what most people expect from this measurement. It is much lower than what most people would expect.

-   **Browser Time**

    It is the time taken by the browser during the transaction. It includes the request and response rendering time at the browser.


It gives a perspective of what is the biggest contributor for the total response time for a transaction. Usually, Server time is high compared to Network and Browser.

**Note:** Review the following if:

-   The server response time is high, then server side components must be reviewed further like business rule, ACL, SQL, Semaphore wait, Session wait time, and others.
-   The network time is high, then transaction components and how much data is being streamed must be reviewed. Recommendation is to keep lightweight transactions with optimal data stream.
-   The browser time is high, then client side scripts/components must be reviewed.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Database performance metrics]()

[Semaphores performance metrics]()

[Event queues performance metrics]()

[ECC Queue performance metrics]()

[Email performance metrics]()

[Scheduler performance metrics]()

[Job details performance metrics]()

[Node health performance metrics]()

[Host health performance metrics]()

[Standby replication Lag]()

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

