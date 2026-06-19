---
title: Configure the Event Management - Insert Health Monitor scheduled job
description: Determine what the Event Management - Insert Health Monitor scheduled job is to monitor. After the job runs, you can view the ServiceNow Event Management application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/EM-insert-health-job.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Self-health monitors for Event Management, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Event Management - Insert Health Monitor scheduled job

Determine what the Event Management - Insert Health Monitor scheduled job is to monitor. After the job runs, you can view the **ServiceNow Event Management** application services.

## Before you begin

Ensure that the **Enable Event Management — self-health monitoring** property is enabled on the Event Management Properties page \(**Event Management** &gt; **Event Management Properties**\).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

2.  Locate and select the **Event Management - Insert Health Monitor** job.

    \[Omitted image "EM-Insert-Health-monitor-job.png"\] Alt text: Event Management - Insert Health Monitor job script execution page

3.  Modify the scripts indicated in the **Run this script** field to determine what the scripts are to monitor.


**Parent Topic:**[Self-health monitors for Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/self-monitoring.md)

