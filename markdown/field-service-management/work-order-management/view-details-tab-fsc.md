---
title: View details screen on the Field Service Contractor for mobile
description: Use Field Service Contractor for mobile application to view work order fields detail.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# View details screen on the Field Service Contractor for mobile

Use Field Service Contractor for mobile application to view work order fields detail.

## Before you begin

Role required: wm\_ext\_agent or wm\_ext\_manager

## About this task

The Details screen shows complete information about a work order task. The contractor agents or managers can use the Details screen to review a work order task to understand the task requirement, and they can Accept or Reject the task. Managers can also reassign the task to a contractor agent.

## Procedure

1.  Access your instance using the ServiceNow Agent mobile application.

2.  Tap **My work**.

3.  Tap **Today's tasks**.

4.  Open any work order task.

5.  On the work order task form, tap **Details**.

6.  On the **Details** tab, review the work order task information shown in the form fields.

    |Field|Description|
    |-----|-----------|
    |Location|The geographical area where an agent executes the assigned task.|
    |Initiated from|Parent task of the work order task.|
    |Asset|Parts required to execute the task.|
    |Scheduled start|The date and time when the work on the task is expected to begin.|
    |Estimated end|Estimated date when the work on the task will end. The date is automatically calculated based on the Scheduled start and Estimated work duration.|
    |Estimated work duration|The estimated time to complete the work. The duration can't exceed the total time of the window. This field is automatically set to an hour. If the task is in the Draft or Pending Dispatch states, you can edit this field.|
    |Work type|The type of work required to complete the task. The available choices are: Break Fix, Install, or Planned Maintenance|
    |Under warranty|Option that indicates a warranty exists for one or more configuration items related to the task.|
    |Description|Detail of the work to be performed at the work location. Complete detail about the problem helps avoid extended communication with the customer in the later stages of the work order life cycle.|
    |Assignment group|Group that has contains the individual agent or vendor to complete the task. By default, this field shows the recommended assignment groups based on the location, asset, and skills for the task. If the field is empty, the system searches for the group covering the territory that includes the location of the task.|
    |Assigned to|Shows the agent or manager currently assigned to the task|


