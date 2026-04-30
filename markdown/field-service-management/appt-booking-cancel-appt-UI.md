---
title: Cancel an appointment from the portal
description: Cancel a service appointment from either the Customer or the Consumer Service Portal.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage an appointment from the portal, Managing appointments in Field Service Management, Using Field Service Management, Field Service Management]
---

# Cancel an appointment from the portal

Cancel a service appointment from either the Customer or the Consumer Service Portal.

## Before you begin

Role required:

## About this task

An appointment cannot be canceled if the current time is within the cancellation time window specified in the service configuration. If within this cancellation time window, the **Cancel** button does not appear in the Appointment field on the work order.

**Note:** Canceling an appointment also cancels the associated work order and work order tasks.

## Procedure

1.  In the portal header, click **Support** &gt; **Appointments** to display the Appointment Listing page.

2.  Click **Upcoming** to view a list of upcoming appointments.

3.  Select the appointment to reschedule.

    This opens the work order for the selected appointment.

4.  Below the **Appointment** field, click **Cancel**.

    The system displays a warning that the appointment and the associated work order will be canceled.

5.  Click **Continue** to cancel the work order.

    The appointment and work order are canceled. The **Appointment** field no longer appears on the work order form and the customer should receive a confirmation email regarding the cancellation.

    Information about the canceled appointment is noted in the **Activities** field on the work order. This information includes the original appointment window, an appointment cancellation message, and the user who made the change.


**Parent Topic:**[Manage an appointment from the portal](../concept/manage-an-appointment-from-the-portal.md)

