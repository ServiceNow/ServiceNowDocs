---
title: Record incidental expenses on the Contractor Portal
description: Agents of contractor companies can use the Field Service Contractor Portal to track incidental expenses that arise during the execution of a work order task.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work order tasks \(WOTs\), Contractor Portal, Completing work orders on the web interface, Use, Field Service Management]
---

# Record incidental expenses on the Contractor Portal

Agents of contractor companies can use the Field Service Contractor Portal to track incidental expenses that arise during the execution of a work order task.

## Before you begin

Role required: wm\_ext\_agent and wm\_ext\_manager

## About this task

Service Management Incidentals or incidental expenses are distinct from other expenses related to work orders, such as part requirements. Incidentals represent expenses that arise during the execution of a task or that are otherwise related to the task. Field Service Management provides incidental types to track the costs of car rentals and miles traveled. Your organization can create additional custom types.

You can create incidental expenses for a work order task at any point during the task life cycle. When an incidental record is created, the system generates an expense line if the following conditions are met:

-   The state is Incurred
-   The type is not None
-   The cost is greater than zero

The expense line is deleted if any of these conditions change.

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor portal** &gt; **My Lists** &gt; **My Tasks**.

2.  Open a work order task from the work order tasks list.

3.  In the Service Management Incidentals related list, click **New**.

4.  On the form, fill in the fields.

5.  |Field|Description|
|-----|-----------|
|Service order Task|\[Read-only\] Work order task number for which you are creating an incidental expense.|
|Type|The type of incidental expense, such as Mileage, Car Rental, or Vendor Cost.|
|Cost|Total cost of the incidental expense.|
|Description|Helpful information about the incidental expense.|
|State|Status of the expense, such as Pending or Incurred.|

6.  Click **Save**.


