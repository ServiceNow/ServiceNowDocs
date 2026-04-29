---
title: Work items in RPA Hub
description: A work item is a record in a work queue that stores the data a robot needs to perform a specific task.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, RPA Hub, Workflow Data Fabric]
---

# Work items in RPA Hub

A work item is a record in a work queue that stores the data a robot needs to perform a specific task.

Each item in the queue is processed separately, allowing robots to handle large workloads in smaller, manageable parts.

-   **Key benefits**
    -   Scalability: Distributes workload across multiple robots.

    -   Resilience: Failed items can be retried without restarting the whole process.

    -   Visibility: Tracks progress and outcomes for each unit of work.

    -   Flexibility: Enables parallel processing of large data sets.


-   **[Manage your work items in RPA Hub](../task/manage-work-queue-items.md#)**  
Manage your work items more efficiently in RPA Hub. You can view your work items, mark them as complete, and reassign a work item.
-   **[Using auto-retry functionality for your failed work items in RPA Hub](auto-retry-wqi-rpa.md)**  
You can use auto-retry functionality in RPA Hub to retry the failed items automatically in your work queue. The retry functionality is based on the **Application** exception type only.

**Parent Topic:**[Using RPA Hub](managing-rpa-hub.md)

