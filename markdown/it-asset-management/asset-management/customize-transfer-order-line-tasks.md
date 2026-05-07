---
title: Customize transfer order line tasks
description: Understand how transfer order line tasks are structured and when to create customized template tasks or subtasks for your organization's asset transfer process.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-04-20"
reading_time_minutes: 1
breadcrumb: [Manage transfer order, Using Asset Management, Asset Management, IT Asset Management]
---

# Customize transfer order line tasks

Understand how transfer order line tasks are structured and when to create customized template tasks or subtasks for your organization's asset transfer process.

When you add a line to a transfer order, a transfer order line task is automatically created for that line. This task represents the first stage in the transfer process for that asset. When you close each task, the next task in the sequence is created, moving the asset through the transfer stages until the line is complete.

Template tasks help you progress through the various stages of the transfer order line. A template task defines the sequence of stages the line must pass through. The template tasks are based on model categories. For example, when you create a customized template task for the Application model category, whenever a transfer order line is created for the Application model category, the template tasks associated with the Application model category are used as transfer order line tasks.

-   **[Create a customized template task](../task/create-customized-template-task.md)**  
Create customized template tasks to configure your specific task workflow for transfer order lines. Default template tasks are available with the Asset Management application. You can’t modify or delete a default template task.
-   **[Create a template subtask](../task/create-template-subtask.md)**  
Create template subtasks to add granularity to the transfer order line tasks. For example, before preparing for shipment, for a computer, you may want to create sub tasks for imaging the computer or adding additional software.

**Parent Topic:**[Manage transfer order](manage-transfer-orders.md)

**Related topics**  


[Transfer order flow](transfer-order-flows.md)

[Transfer order tasks](work-with-transfer-orders.md)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md)

