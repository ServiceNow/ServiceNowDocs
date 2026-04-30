---
title: Delegate reservations in Microsoft Outlook add-in
description: Delegate additional permissions to read, create, or change items in your Microsoft Outlook mailbox. Delegate access to a colleague or team member. Delegates can create and reserve resources \(desks, rooms, equipment, services like catering\) for other employees.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 2
breadcrumb: [Using Workplace Reservations for Microsoft Outlook Add-in, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Delegate reservations in Microsoft Outlook add-in

Delegate additional permissions to read, create, or change items in your Microsoft Outlook mailbox. Delegate access to a colleague or team member. Delegates can create and reserve resources \(desks, rooms, equipment, services like catering\) for other employees.

## Before you begin

When you grant a delegate access, you can determine the level of access that the delegate has to your calendar or mail folders. You can grant a delegate permission to read items in your folders or permission to read, create, change, and delete items.

Role required: admin

## Procedure

1.  Open the Microsoft Outlook application.

2.  Select the **Calendar** &gt; **People's calendar** to select a team member's calendar to who you want to delegate access to your calendar.

    For example: Select Wednesday Addams' calendar. Here, Sarah Rivera is the meeting organizer who has provided Wednesday Addams the delegation rights to Sarah's calendar.

3.  Select a date on the calendar, select and hold \(or right-click\) to select **New event**.

    You can also select a date and double-click to open the New Event calendar invite form.

4.  On the New Event form, fill in the required information.

    For more information, see [Create a reservation in Microsoft Outlook add-in](outlook-create-rsv.md).

5.  Select the add-in manifest file of your instance and create a reservation using the Make a reservation form.

    For more information, see [Create a reservation in Microsoft Outlook add-in](outlook-create-rsv.md).

6.  Review your reservation in the Reservation Summary page.

    ![Reservation summary showing the Reservation organizer and on behalf of (employee with delegate access).](../image/rsv-summary-page-use-for-delegate-summary3.png)

7.  Select **Send** to send the meeting invite.

    **Note:** An event or meeting invite when it’s initially created in Microsoft Outlook is in a **Draft** state. When the meeting invite is sent, it is sent to the Microsoft Exchange Online server. It takes some time for a meeting or reservation request sent from the client server to be synchronized with the Microsoft Exchange Online server. After synchronization, the reservation changes to **Confirmation** state.

8.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **All Reservations**.

    Select your reservation to review the details on Workplace Reservation Management.

    If you have delegated access to create a reservation, the All Reservations page shows the reservation details along with updated **Requested for** and **Opened by** column values.

    ![Workplace Reservations page showing updated reservations for an employee. If you have provided delegate access, it shows the column values for the delegate and the organizer.](../image/delegate-fields-all-reservations-page.png)


**Parent Topic:**[Using Workplace Reservations for Microsoft Outlook Add-in](../concept/using-outlook-addin.md)

**Previous topic:**[Edit reservation details in Microsoft Outlook](outlook-edit-rsv.md)

**Next topic:**[Analytics and Reporting Solutions for Workplace Reservation Management](../concept/analytics-reporting-for-rsv-mgmt.md)

