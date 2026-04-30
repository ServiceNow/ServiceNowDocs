---
title: View host data collection for an agent
description: Run data collection on an agent's host to discover the components that are running on the host.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enabling ACC data collection, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# View host data collection for an agent

Run data collection on an agent's host to discover the components that are running on the host.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

The Refresh Host Data for Agents scheduled job collects host data and runs every hour on the following:

-   Hosts which have not been discovered in the past 12 hours.
-   Host for which Discovery failed.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

    In the **Host data collection** column, view the status of data collection on the agent's host. The possible statuses are:

    |Status|Description|
    |------|-----------|
    |&lt;empty&gt;|Indicates that the agent has been added within the past minute and the Refresh and Publish Monitoring Policies scheduled job has not yet run to initiate data collection. The job runs every minute.|
    |Collected \(green\)|Host data collection is complete.|
    |Collecting \(yellow\)|Host data collection is in progress.|
    |Collection failed \(red\)|Host data collection failed.|

2.  Locate the **Host data last collected** column to view when data collection was last performed on the host.


**Parent Topic:**[Enabling Agent Client Collector data collection](../concept/data-collection-enabling.md)

