---
title: Case action status logging
description: Logging for the case action status feature uses a metric definition to view information about blocking tasks associated with customer service cases.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-09-22"
reading_time_minutes: 1
breadcrumb: [Case action status overview, Administer Customer Service Management, Customer Service Management]
---

# Case action status logging

Logging for the case action status feature uses a metric definition to view information about blocking tasks associated with customer service cases.

Defined metrics can track how long a specific field holds a certain value. The **Case Actor Duration** metric definition logs the events related to case blocking tasks.

When a case blocking task is created or resolved, the system logs the information. This information can be used to report on the duration of the case with the customer, the agent, or other internal stakeholders.

As a case gets blocked and unblocked by a customer or an internal user, the metric definition tracks the duration of the case with each of these actors.

The metrics include:

-   Case number
-   Metric definition
-   Value
    -   Needs attention
    -   Blocked by customer
    -   Blocked internally and by customer
-   Start and end times
-   Duration

To access the **Case Actor Duration** metric definition, navigate to **All** &gt; **Metrics** &gt; **Definitions** and select the definition from the list. For more information about metric definitions, see the following topics:

-   [Metrics](https://www.servicenow.com/docs/access?context=c_MetricDefinitionSupport&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)
-   [Define a metric](https://www.servicenow.com/docs/access?context=create-metric&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

**Parent Topic:**[Case action status overview](../concept/customer-service-case-action-status.md)

