---
title: Queue implementation in RPA Hub
description: In RPA Hub, the queues are implemented to distribute the workload among various robots. Work Items \(WI\) within a queue are processed simultaneously by two or more robots.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Queue implementation in RPA Hub

In RPA Hub, the queues are implemented to distribute the workload among various robots. Work Items \(WI\) within a queue are processed simultaneously by two or more robots.

## Queue implementation overview

A queue is a repository that can hold a number of work items. Work items can store multiple types of data, such as transaction information, customer details, or information from a document.

A queue refers to a structured data storage mechanism used to manage and control the distribution of tasks, work items, or cases to different robots for processing. RPA queues play a crucial role in orchestrating the execution of automated processes and ensuring that tasks are processed efficiently, accurately, and in the desired order.

Queues facilitate task distribution, coordination, and efficient processing across multiple bots or processes. Queues are particularly useful in scenarios where automation needs to handle a dynamic workload with different tasks arriving at different times, such as processing incoming emails, customer orders, or data entries.

In RPA Hub, you cannot delete a queue that is associated to a published bot process.

## Work item lifecycle

The State transition of a work item guides you through the stages of its life cycle.

1.  Work items are created from upstream systems using the **Add WorkItem to Queue** flow action or by robots, using the **CreateStringWorkItem** or **CreateJSONWorkItem** component.
2.  Using the **PickWorkItem** component, robots pick a work item for processing.
3.  After a work item is picked, the robot is stamped on the work item.

    **Note:** No other robot can pick this work item.

4.  Work items are processed by the criteria that you specified. There are various conditions to determine which item must be picked and it varies for each automation. This criterion is the input for the **PickWorkItem** component.
5.  After a work item is picked, the robot updates it multiple times while processing it using the **UpdateWorkItem** component.

    This robot can also release this work item by partially processing it, so that other robots can pick it. This process is performed by the input in the **ReleaseMode** field, in the **UpdateWorkItem** component.

6.  After the robot completes the processing, it updates the work item to complete using the **UpdateWorkItem** component and picks the next work item that is Step 2.

The following diagram shows the lifecycle of work items \(WI\) in RPA Hub application.

![Lifecycle of work items in RPA Hub.](../image/wqi-lifecyle.png "Lifecycle of work items (WI) in RPA Hub")

**Related topics**  


[Create a queue in RPA Hub](../task/create-queue.md)

[Assign a bot process to a queue from Queues menu](../task/assign-botprocess-queue.md)

[Manage your work items](../task/manage-work-queue-items.md)

[Using auto-retry functionality for your failed work items in RPA Hub](auto-retry-wqi-rpa.md)

[Queue form in RPA Hub](../reference/queue-form.md)

[Work item form in RPA Hub](../reference/work-queue-form.md)

[Queue](../../rpa-studio/concept/queue-connector.md)

