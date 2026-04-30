---
title: Create an HR case for a lifecycle event
description: Create a lifecycle event case. A lifecycle event case is an HR case that is fulfilled by a lifecycle event. For example, the HR service for New Hire Onboarding is fulfilled by the lifecycle event for New Hire Onboarding.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Create an HR case for a lifecycle event

Create a lifecycle event case. A lifecycle event case is an HR case that is fulfilled by a lifecycle event. For example, the HR service for New Hire Onboarding is fulfilled by the lifecycle event for New Hire Onboarding.

## Before you begin

Role required: sn\_hr\_le.case\_writer

A lifecycle event administrator must have built the lifecycle event and created a corresponding HR service before you can create a case for that event. See [Building a lifecycle event](../concept/hr-lifecycle-event-configuration.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Create New Case**.

2.  In the **Search for Employee** field, select the employee you are creating the case for.

    **Note:** You can search by employee name, partial employee name, case number, or any indexed field on the HR Profile of the sys\_user table.

3.  On the HR case creation form, under the **Case Details** section, select the HR service you are requesting for the employee.

4.  Click **Create Case** to create the HR case.

5.  On the HR case form, fill in the fields on the form, as appropriate.

    For further details on the form fields, see [Work an HR case](t_CreateAnHRCase.md).

6.  Click **Ready for Work** to change the state from **Draft** to **Ready**.


## What to do next

After you create a lifecycle event case, you can track the case's progress and monitor the status of the individual activity sets and activities.

The following GIF shows an example of an in-progress lifecycle event case.

**Note:** You can drill down from the lifecycle event case list view to monitor the status of the individual activity sets and activities. You can also drill down from the individual event case form.

