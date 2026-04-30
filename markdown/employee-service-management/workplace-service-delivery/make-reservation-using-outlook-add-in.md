---
title: Make a reservation using Workplace Reservations for Microsoft Outlook Add-in
description: Schedule an event or appointment in the Microsoft Outlook using the additional features provided by the Workplace Reservations for Microsoft Outlook Add-in application.
locale: en-US
release: yokohama
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Workplace Reservations for Microsoft Outlook Add-in, Workplace Service Delivery, Employee Service Management]
---

# Make a reservation using Workplace Reservations for Microsoft Outlook Add-in

Schedule an event or appointment in the Microsoft Outlook using the additional features provided by the Workplace Reservations for Microsoft Outlook Add-in application.

## Before you begin

-   [Create a manifest file for Microsoft Outlook Add-in](add-manifest-file-for-outlook-addin.md).
-   Upload the manifest file. Perform any one of the following actions depending on the usage:
    -   [Upload the manifest file for a single user](upload-manifest-for-single-user.md).
    -   [Upload the manifest file in Microsoft Office 365](upload-the-manifest-file-office365.md).

Role required: admin

## Procedure

1.  Open **Microsoft Outlook** application.

2.  Perform any one of the following actions depending on what type of reservation you want to make:

    -   To create an appointment or event, navigate to **New items** &gt; **Appointment**.
    -   If you want to send a meeting invite, navigate to **New items** &gt; **Meeting**.
3.  In the Appointment window, select the reservation add-in.

    The add-in opens a side-bar that contains a reservation form.

    **Note:** The name of the add-in depends on the name specified in the manifest file.

4.  Select a date and time for the reservation.

    If **Max days in future** is enabled, and if the start date and end date exceeds the **Max days in future** value, a warning message is displayed to show that reservation can only be made up to the number of days specified in **Max days in future**. The **Max days in future** value is configured on the Reservable module and specifies the maximum number of the days in the future up to which the Reservable module can be reserved.

    **Note:** If the **Max days in future** value is not enabled, users can select a date as per the **Max number of occurrences** on the Reservable module. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

    -   If an employee clicks open the calendar icon ![date picker icon](../../workplace-visitor-mgmt/image/date-time-icon.png) and tries to select a date greater than the **Max days in future** value, the dates are disabled in the calendar date picker.
    -   For example, if the **Max days in future** value is 90 days, and if you try to select a date beyond 90 days, then the number of days beyond 90 days is disabled in the calendar date picker.
    -   A warning message is shown that you can reserve a space within the next 90 days only. The date defaults to the current date.
    -   If an employee manually enters a date that is greater than what is specified in the **Max days in future** value, then the application resets the date to the current date.
    **Note:** If the number of days for a reservation exceeds the **Max days in future** value, the **Save Reservation** and **Add extra services** options are disabled. The employee is not able to save the selected services. The employee can send out the invitation through Outlook, but no services are added.

5.  In the Reserve a space sidebar, fill in the following fields:

    1.  Select the **Building** in which you want to make an appointment.

    2.  Select the **Floor** in which you want to reserve a space for the appointment.

    3.  Select the required **Capacity**capacity of the space.

        The spaces will be displayed depending on the capacity specified.

6.  Click **Search**.

    The available spaces are displayed based on the search.

7.  Select a space from the list of available spaces.

    You can also select multiple spaces.

8.  If you have selected multiple spaces, to mark all the space details as private, select **Make all space details private**.

    **Note:** The option is displayed based on the privacy settings set on the selected spaces.

9.  If you have selected multiple spaces, to set privacy for a space individually, use the **Make space details private** option placed below each space.

    **Note:** The option is displayed based on the privacy settings set on the space.

10. Click **Save and next**.

11. Click **+Add extra services** to request extra services along with your reservation.

12. If you have selected multiple spaces, select **+Add extra services** under each space separately.

13. In the services form, select from the following services:

    -   **Catering**: Option to request food services. Specify breakfast and/or lunch preferences and the quantity required.
    -   **Equipment**: Option to request any special equipment for the meeting.
14. Click **Save services**.

15. Review your reservation details.

16. To edit your reservation, click **Change reservation**.

17. To edit the extra services requested, click **+Add/manage extra services**.

18. Click **Save reservation**.

    The reservation is created and logged in the Workplace Reservation Management application.

19. In the Outlook appointment window, click **Send** to send the meeting request.

    The meeting request will be sent to the selected spaces to confirm the reservation.

    **Note:** If Workplace calendar synchronization is installed and personal authentication mode is enabled, a pop-up notification appears if a user does not have a token while attempting to reserve a sync-enabled room. The notification informs the user that the token is not available and instructs them to log in to Microsoft Exchange with the respective email to retrieve the token.


## Result

The reservation is created. The reservation is sent only if you send the invite from the Microsoft Outlook window.

