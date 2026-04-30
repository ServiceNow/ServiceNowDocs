---
title: Queues for Recommendation Actions Application
description: Admins and Recommended Actions administrators can configure queues to manage the asynchronous evaluation of recommendations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Queues for Recommendation Actions Application

Admins and Recommended Actions administrators can configure queues to manage the asynchronous evaluation of recommendations.

## Access Path and Role Requirements

To view or manage the queue, navigate to the following location in the application:

Navigate to **All** &gt; **System Policy** &gt; **Queue Registry**

Required Roles: admin or sn\_nb\_action.next\_best\_action\_admin.

## Default Queue Configuration

The Recommended Actions application includes a preconfigured queue by default, for processing actions efficiently.

-   Queue Name: sn\_nb\_action.ra\_processor\_queue\_1
-   Scale Factor: 2
-   Polling Interval: 5 seconds

## Optimizing Queue Configuration for Lower Latency

To enhance responsiveness and reduce latency in action processing, consider increasing the Scale Factor, such as from **2** to **3**

-   Queue Name: sn\_nb\_action.ra\_processor\_queue\_1.
-   Updated Scale Factor: 3
-   Polling Interval: 5 seconds

## Considerations for Scaling

Increasing the Scale Factor enables the queue to process more items concurrently and reducing latency. However, it also increases demand on system resources such as CPU and memory.

