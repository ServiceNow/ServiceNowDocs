---
title: Using Clinician Portal to find and manage vaccination appointments for users
description: As a user with the sn\_vaccine\_sm.clinician role, you can find vaccination appointments for users, view all of their upcoming appointments for a particular location, view, and work on a vaccination record, mark an appointment as a no-show, cancel an appointment, and more, all from within a single portal.
locale: en-US
release: xanadu
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Using Clinician Portal to find and manage vaccination appointments for users

As a user with the sn\_vaccine\_sm.clinician role, you can find vaccination appointments for users, view all of their upcoming appointments for a particular location, view, and work on a vaccination record, mark an appointment as a no-show, cancel an appointment, and more, all from within a single portal.

![Vaccine Administration Management clinician portal landing page where users can manage appointments, scan QR codes to find appointments, and view a calendar of all appointments.](../image/vam-clinician-portal-landing-page-v5.1.png "Clinician portal")

**Note:** The clinician portal is optimized for both tablet and mobile. However, the mobile view does not currently support the selection of more than one appointment at a time for bulk updates.

## Find vaccination appointments

<table id="table_ew2_4hb_m4b"><thead><tr><th>

Description

</th><th>

Screen

</th></tr></thead><tbody><tr><td>

Clinicians can find vaccination appointments by scanning the user's QR code, entering the code manually, or looking up the appointment in the portal.

 Clinicians can view the appointments for a particular location from the list. To view all upcoming appointments, click **See all appointments**. Upcoming appointments include all appointments for that day at the selected location, as well as appointments from the previous hour. For example, if the clinician views the upcoming appointments at 9:00 AM, they see all the assigned appointments from 8:00 AM through the end of the day.

 Once the clinician selects a location, it remains selected throughout the session.

</td><td>

![The Manage your appointments view which displays the user's upcoming appointments.](../image/vam-clinician-portal-find-appointments-v5.1.png)

</td></tr></tbody>
</table>## View and search appointments

<table id="table_mx1_b3b_m4b"><thead><tr><th>

Description

</th><th>

Screen

</th></tr></thead><tbody><tr><td>

From the list view, clinicians can view all appointments for a particular location, search for users by name, and filter for appointments. By default, the dates for appointment filters are set for a week's time.

**Note:** Using the search by name filter, clinicians can view only the appointments booked for the registered users. However, the clinician can still scan the QR code of an internal user and can administer the vaccine.

</td><td>

![List view of appointments, filtered by date range and organized by name, appointment date and time, code, vaccine, and status.](../image/vam-clinician-portal-appointment-list-view-v6.png)

</td></tr></tbody>
</table>## View and work on an appointment

<table id="table_cr4_5fb_m4b"><thead><tr><th>

Description

</th><th>

Screen

</th></tr></thead><tbody><tr><td>

Clinicians can view and work on an appointment record, including:

-   Verify the user's ID
-   Verify the user's details
-   Fill in screening questions
-   Verify that the vaccine is administered properly.

If there are multiple vaccines booked under the same appointment and if the clinician has administered only one, details can still be captured by the clinician. Later, the user can book the vaccine that was not administered.

-   Provide comments and work notes
-   Verify that the user has verbally consented to the vaccine
-   Verify that the user was provided with information about the vaccine
-   Assign an appointment to oneself
-   Mark an appointment as a no-show
-   Cancel an appointment
-   Mark an appointment as complete

**Note:** When the clinician marks a vaccination appointment as complete, an immunization record creates for the user and stores on the Immunization \(sn\_hcls\_immunization\) table.


</td><td>

![The appointment details view which displays patient information and vaccination appointment cases.](../image/vam-clinician-portal-appointment-details-v5.png) ![The appointment details view which displays patient information and vaccination appointment cases.](../image/vam-clinician-portal-appointment-details-02:22.png)

</td></tr></tbody>
</table>**Parent Topic:**[Using Vaccine Administration Management](using-vaccine-administration-management.md)

