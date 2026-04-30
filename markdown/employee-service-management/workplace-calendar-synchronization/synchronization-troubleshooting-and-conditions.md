---
title: Synchronization - Prerequisites and implementation
description: When you connect to your calendar provider for synchronization, you may incur a few connection or synchronization-related issues.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Manage calendar synchronizations, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Synchronization - Prerequisites and implementation

When you connect to your calendar provider for synchronization, you may incur a few connection or synchronization-related issues.

## Synchronization prerequisites

When you synchronize reservations, it is important to know the following:

-   You can’t edit a reservation that is created using the calendar provider in the Workplace Reservation Management application.
-   During reservation synchronization, only the notes added to the reservation using the Workplace Reservation Management application is considered. That is, if the body of the reservation is updated in Microsoft Exchange, those updates are not synchronized back to Workplace Reservation Management.
-   When you create, update or delete a reservation, it’s performed directly on the employee's calendar. During synchronization, the events are read from the resource calendar, that is, the room calendar.
-   If an event is rejected or declined by the calendar provider resource, in such case the reservation remains in the Awaiting confirmation state. For the same reason, a scheduled job **Clean-up Awaiting/Rejected Reservations** is available that you can run on any suitable frequency to clear the reservations that are rejected or declined
-   For Microsoft Exchange Online, after synchronization, ensure that the meeting subject is unchanged. If the meeting subject is changed, use Microsoft PowerShell to make changes. For more information, refer to [https://learn.microsoft.com/en-us/exchange/troubleshoot/client-connectivity/calendar-shows-organizer-name](https://learn.microsoft.com/en-us/exchange/troubleshoot/client-connectivity/calendar-shows-organizer-name).

## Synchronization implementation

-   **Rooms and spaces**

    While performing reservation synchronization, you can synchronize both rooms and spaces.

-   **Invitees**

    Invitees of a reservation can be synchronized in both the ways, that is, from Workplace Reservation Management to the calendar provider or vice versa.

    -   If the reserved room has reservation synchronization enabled, then the details of the reservation are sent to the invitees from their calendar provider such as Google or Microsoft Exchange.
    -   When synchronizing a reservation with invitees, the application performs the following:
        -   The application checks if the invitees are known users, or visitors and categorizes in the reservation accordingly.
        -   If an invitee isn’t a known user or a visitor, then they are categorized as “External” in the reservation. The details of these invitees aren’t displayed on the Reservation summary.
        -   The invitees receive a notification when a reservation is changed or updated in the Workplace Reservation Management application. However, a notification is not received if the reservation is created or updated in the calendar provider.
-   **Notes**

    If a note is added in a reservation created in the Workplace Reservation Management application, it is saved on the reservation record. An employee can update a note when required. The reservation summary page displays the summary of the meeting note. When this reservation \(with notes\) is synchronized, then the following actions are performed in the calendar provider:

    -   The notes are added to the body of the meeting email.
    -   If there are any notes added to the reservation from the calendar provider, it is overwritten with the notes added using the Workplace Reservation Management application when there is a reservation update.
    -   During reservation synchronization, only the notes added to the reservation using the Workplace Reservation Management application is considered. That is, if the body of the reservation is updated in Microsoft Exchange, those updates are not synchronized back to Workplace Reservation Management.
-   **Privacy**

    If an employee reserves a room using their calendar provider, then the privacy of the reservation depends on the privacy setup made on the building to which the space or room belongs. The privacy of such reservations can be changed or overridden using Workplace Reservation Management or Workplace Service Delivery for Mobile.

-   **Virtual meeting link**

    If a reservation is created in Microsoft Exchange using Zoom or Microsoft Teams, during synchronization, the meeting link is retrieved and added to the reservation record in Workplace Reservation Management as a virtual meeting link. However, it is dependant on whether the virtual meeting provider is configured in Workplace Reservation Management or not. If it is not configured, then the meeting link is not included.

    When a Workplace Reservation Management reservation includes a virtual meeting link, then the meeting links appear as follows when it’s synchronized with the Microsoft Exchange calendar of the attendees:

    -   **Zoom**: If a Zoom meeting link is added, the link appears in the **Location** field of the email containing the meeting invite.
    -   **Microsoft Teams**: If a Microsoft Teams link is added, the meeting link and the joining-related details are added to the body of the calendar event. Similarly, when a reservation is created in the Microsoft Exchange calendar using the **Teams meeting** toggle button, the meeting link is retrieved and saved as a virtual meeting link on the reservation record in Workplace Reservation Management application.

        **Note:** As the meeting link appears in the body of the email, in any case, if you want to update or change the meeting details, you must do it only using the Workplace Reservation Management. Because when a reservation synchronization is performed, the details \(in this case, the meeting link and details\) are synchronized only in one way, that is, from Workplace Reservation Management to the calendar provider \(in this case Microsoft Teams\). If you already change the meeting details or the notes from the calendar provider, it is overwritten by Workplace Reservation Management when a synchronization is performed.

    -   **Any other virtual meeting providers**: The meeting link is added in the **Location** field of the email containing the meeting invite.
    To set up Microsoft Teams, refer to [Connect Workplace Reservation Management with Microsoft Teams](../../wsd-reservation-management/task/connect-rsv-mgmt-with-teams.md).

    To set up Zoom, refer to [Connect Workplace Reservation Management with Zoom](../../wsd-reservation-management/task/connect-rsv-mtm-with-zoom.md).


## Debugging, handling throttling and other

**Debug Workplace Service Delivery to Microsoft Exchange Online**:

**Note:** Ensure that Developer Trace is to be enabled for debugging. Navigate to **Process Automation Designer** &gt; **Properties**. Set the **Level of reporting data generated by the flow engine** flow designer properties to **All configuration and runtime values \(For debugging only\)**.

1.  Check for events in **Workplace Calendar Synchronization** &gt; **Synchronization** &gt; **Events** &gt; **.**
2.  Ensure that all the events are processed successfully and their Response has “Event ID” &amp; “Icaluid”.
3.  If an event fails with “Too many requests” error, enable **WSDR Reprocess Events** scheduled job with a 5-minute frequency.
4.  For an exact response message from “Rest”, navigate to **Flow Designer** &gt; **Executions**. Apply the filter by the name “Create Calendar Event”.
5.  For any other external error above the 400 error code, validate the setup on the Azure Portal according to the error code. Following are the most common errors:
    -   Access to oData is inactive
    -   Invalid Object
6.  To fix these errors, the resource or the user must be in the scope of tenant Id\(Client Id\)

**Debug Microsoft Exchange Online to Workplace Service Delivery**

1.  Make sure that the **Create and Update Reservations from Events** scheduled job is active.
2.  Verify that there is an event entry in **Microsoft Exchange Online Spoke** &gt; **Events**.
3.  If there is no entry, validate. Navigate to **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Reservable Sync Configuration** &gt; **.**.
4.  Verify if the room email is active.
5.  Check if the subscription field is populated and verify if that subscription status is active and the status is 200.
6.  If the subscription is not populated, deactivate and activate the individual reservable sync configuration record.
7.  If the subscription is still not populated, then navigate to **Flow designer** &gt; **Executions** &gt; **Create or Update Subscription** and validate the flow.
8.  If there is an issue with the resource, you may see errors like resource not found, invalid Resource, the SMTP address has no mailbox associated with it or others. The error might have occurred for the below reasons:
    -   Invalid email ID
    -   Must have proper resource mail box in office.com
    -   Resource/User must be in scope of tenant Id\(Client Id\)
9.  For more information on the errors, check [https://learn.microsoft.com/en-us/graph/errors](https://learn.microsoft.com/en-us/graph/errors) and fix the root cause.

**Throttling issue \(HTTP Error 429\) in Microsoft Exchange Online while processing huge reservations:**

If you are processing huge reservation requests at a time, there might be a throttling on Microsoft Exchange, that is, you might incur HTTP Error 429. In such cases, it is recommended that you configure the Retry policies in the Integration Hub application. Perform the following actions to configure:

1.  Go to **IntegrationHub** &gt; **Retry Policies**.
2.  Select **MS Exchange Online HTTP Retry Policy**.
3.  In the **Retry Strategy** field, select **Honor "Retry-After" Header**.
4.  In the **Max Elapsed Time \(seconds\)**, set the value to 120.

    **Tip:** Set the value to 120 or above.


**Parent Topic:**[Manage calendar synchronizations](../concept/manage-calendar-synchronizations.md)

**Related topics**  


[View synchronization details](../task/view-synchronization-details.md)

[Events in Workplace Calendar Synchronization](events-in-workplace-calendar-synchronization.md)

[Run Instance scan to check Microsoft Exchange Online synchronization configuration](../task/run-instance-scan-on-your-workplace-cal-sync-configs.md)

