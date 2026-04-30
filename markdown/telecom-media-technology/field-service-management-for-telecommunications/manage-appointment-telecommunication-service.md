---
title: Managing the appointments for telecommunication services
description: Manage the appointments for the field services to enable the installation, activation, and site assessments that are needed for connectivity services.
locale: en-US
release: xanadu
product: Field Service Management for Telecommunications
classification: field-service-management-for-telecommunications
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field Service Management for Telecommunications, Telecommunications, Media, and Technology]
---

# Managing the appointments for telecommunication services

Manage the appointments for the field services to enable the installation, activation, and site assessments that are needed for connectivity services.

With the use of the ServiceNow Telecommunication Open API \(com.sn\_tmf\_api\) application, you create appointments from your system for the connectivity-related field services. You can book an appointment on an existing work order and assigned it to the field service agent. To learn more about booking appointments, see [Managing appointments in Field Service Management](https://www.servicenow.com/docs/access?context=managing-appointments-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

This feature supports the following:

-   Returns the available time slot within a provided time period for which you can book appointments.
-   Enables you to book appointments for a work order with start and end times and available slots.
-   Reschedule appointments with a different time slot for a  work order.
-   Cancel the appointment with a given ID for a  work order.

The Telecommunication Open API application uses the Appointment Open API to support the external system to create and manage appointments for the field services. This API is a ServiceNow® implementation of the Open API TMForum TMF646 Appointment API specification.

To learn more about the methods used to book and manage appointments, see [Appointment Open API](https://www.servicenow.com/docs/access?context=appointment-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Configuring the appointment booking feature

To manage appointment bookings in your system, you must create, modify, or enable the application configuration and the individual service configurations. Do the following steps to configure the appointment booking feature:

1.  [Configure an appointment booking record producer](https://www.servicenow.com/docs/access?context=appt-booking-config-record-producer&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).
2.  [Create or modify an appointment booking service configuration](https://www.servicenow.com/docs/access?context=appt-booking-create-service-config&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).
3.  [Configure variable in service catalog record producer for appointment booking](https://www.servicenow.com/docs/access?context=create-variable-in-catalog-record-producer-for-appoinment-booking&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

