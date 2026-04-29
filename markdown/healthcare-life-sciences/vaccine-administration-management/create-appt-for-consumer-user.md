---
title: Schedule an appointment
description: Schedule vaccination appointments on behalf of the consumer user.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage user appointments as a clinician or a vaccine agent, Use Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Schedule an appointment

Schedule vaccination appointments on behalf of the consumer user.

## Before you begin

Role required: sn\_vaccine\_sm.clinician

**Note:** A clinician or a vaccine agent can’t create an appointment on behalf of internal users.

## Procedure

1.  Navigate to **All** &gt; **Vaccine Administration Management** &gt; **Agent** &gt; **Search Assist**.

2.  Select **Consumer**.

3.  Search for the new consumer user record using the search options provided such as first name, last name, and phone, and click **Search**.

    You can find the new information record under Personal information.

4.  Select the record to book an appointment.

5.  From the consumer user record, select **Book Vaccine Appointment**.

    The **Book Vaccine Appointment** button isn’t visible for the internal user.

6.  Schedule the vaccination appointments by choosing your preferred method and site for vaccination.

    You can either choose the same vaccination site for both doses, or you can choose a different vaccination site for each dose. To choose from your preferred vaccination method while scheduling or rescheduling your appointments, the **sn\_vaccine\_sm.allow\_user\_selection\_of\_vaccine\_method** system property value must be set to **true**. For details on how to configure multi-vaccine appointment bookings, see [Multi-vaccine appointment bookings configuration](../concept/multi-vaccine-appointment-bookings-configuration.md).

7.  Fill in the required details, and click **Submit**.

    The vaccination appointment is scheduled for the user and separate emails for both vaccination appointments are shared with the user.

8.  Click **Close**.

    In the Appointment related list, two separate vaccination tasks are created.


**Parent Topic:**[Manage user appointments as a clinician or a vaccine agent](../concept/user-appt-mngt-clinicans-agents.md)

