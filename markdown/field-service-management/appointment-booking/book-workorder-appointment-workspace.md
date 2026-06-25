---
title: Book work order appointment in the CSM Configurable Workspace
description: Book appointment for an associated work order or work order task to dispatch agent to address the customer issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/appointment-booking/book-workorder-appointment-workspace.html
release: australia
product: Appointment Booking
classification: appointment-booking
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing appointments in the CSM Configurable Workspace, Managing appointments on behalf of a customer, Managing appointments, Use, Field Service Management]
---

# Book work order appointment in the CSM Configurable Workspace

Book appointment for an associated work order or work order task to dispatch agent to address the customer issue.

## Before you begin

Role required: wm\_qualifier and sn\_customerservice\_agent, or wm\_qualifier and sn\_customerservice.consumer\_agent

Setup the **Field Service Order Configuration** to book an appointment for work orders and **Field Service Task Configuration** to book an appointment for work order tasks. For more information, see [Configuring Appointment Booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/appointment-booking-administer.md).

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Click the List icon \(\[Omitted image "ListIcon.png"\] Alt text: List icon.\).

3.  Open either work order or work order task.

    -   To book an appointment for a work order, navigate to **Work Orders** &gt; **Created by me**, and then select the desired work order.
    -   To book an appointment for a work order task, navigate to **Work Order Tasks** &gt; **Created by me**, and then select the desired work order task.
4.  To book an appointment:

    1.  Click **Book Appointment**.
    2.  In the **Schedule appointment** dialog box, view available appointment time slots, and then select the desired day and time.
    3.  Click **Schedule**.
    The application books an appointment for the work order or the work order task depending upon your selection.


**Related topics**  


[Reschedule work order appointment in the CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/appointment-booking/Reschedule-workorder-appointment-workspace.md)

[Cancel work order appointment in CSM Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/appointment-booking/Cancel-workorder-appointment-workspace.md)

