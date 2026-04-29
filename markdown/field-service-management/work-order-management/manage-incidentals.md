---
title: Enter incidental expenses directly from a work order task on a mobile device
description: Create and track incidental expenses that arise during the execution of a work order task through the Field Service Contractor for mobile application.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Enter incidental expenses directly from a work order task on a mobile device

Create and track incidental expenses that arise during the execution of a work order task through the Field Service Contractor for mobile application.

## Before you begin

Role required: wm\_ext\_agent or wm\_ext\_manager

## About this task

Incidental expenses are expenses related to work orders that arise during the execution of a task or are otherwise related to the task, such as vendor or mileage costs, but are not standard predicted expenses such as part requirements.

You can create incidental expenses for a work order task at any point during the task life cycle.

## Procedure

1.  Access your instance using the ServiceNow Agent mobile application.

2.  On the **My work** navigation tab, tap **Today's tasks**.

3.  Open a work order task from the list.

4.  On the **Details** tab, tap the More actions \(![More actions icon](../image/OverflowIcon.png)\) icon.

5.  Tap the **Log incidental** function.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|The type of the incidental expense, such as Mileage, Car Rental, or Vendor Cost.|
    |Cost|Total cost of the incidental expense.|
    |Description|Helpful information about the incidental expense.|
    |State|Status of the expense, such as Pending or Incurred.|
    |Attachment|Option to include any supporting attachments.|

7.  Tap **Submit**.


## Result

The incidental is created and can be accessed from a work order Related tab or My incidental navigation tab.

The system generates an expense line for the incidental expense if the following conditions are met:

-   The state is Incurred
-   The type is not None
-   The cost is greater than zero

If any of the conditions change, the expense line is deleted.

