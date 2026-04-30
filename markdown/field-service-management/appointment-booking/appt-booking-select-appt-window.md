---
title: Select an Appointment window
description: To book or reschedule an appointment for a service, use the Select Appointment pop-up window. To see what time slots are available, choose your preferred day and time, and then submit your appointment request.
locale: en-US
release: yokohama
product: Appointment Booking
classification: appointment-booking
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage appointments from a work order or work order task, Manage appointments on behalf of a customer, Manage appointments, Using Field Service Management, Field Service Management]
---

# Select an Appointment window

To book or reschedule an appointment for a service, use the Select Appointment pop-up window. To see what time slots are available, choose your preferred day and time, and then submit your appointment request.

In the Select Appointment pop-up window, see appointment availability based on the configurations created for the application and the selected service. This configuration can include:

-   Whether the window shows available appointments in a day or week view
-   The length of the appointment windows \(for example, two hours\).
-   The start and end times for the appointment windows.
-   Recommendation configuration for seismic appointment booking calendar and appointment booking slot recommendation.
-   The number of appointments available every day.

    **Note:** Based on the configuration set for the user's time format, the appointment booking window displays either a 12-hr or a 24-hr clock.


A read-only field at the top of the window displays the currently selected day or week. Use the arrows or the calendar icon at the top of the window to display different dates. Unavailable appointment windows are grayed out and not selectable.

If you have enabled seismic appointment booking calendar and appointment booking slot recommendations, you see a common selection window across all interfaces. The seismic appointment booking calendar adds a **Recommended** banner to suggest appointment slots.

The time zone used for appointment is displayed in the lower corner of the window.

-   If the selected location for the service has an associated time zone, that time zone is used.
-   If the location doesn’t have an associated time zone and the current user does, the user's time zone is used.
-   If the location and the current user don't have an associated time zone, the system time zone is used.

**Parent Topic:**[Manage appointments from a work order or work order task](../concept/managing-appts-from-work-order.md)

**Related topics**  


[Personalize the system time format](https://www.servicenow.com/docs/access?context=t_PersonalizeTheSystemTimeFormat&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

