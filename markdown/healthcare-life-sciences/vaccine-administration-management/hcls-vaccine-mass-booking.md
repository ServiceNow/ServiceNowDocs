---
title: Mass book vaccine appointments
description: Schedule appointments for multiple users at the same time instead of having users individually request appointments in the self-service portal.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Mass book vaccine appointments

Schedule appointments for multiple users at the same time instead of having users individually request appointments in the self-service portal.

## Before you begin

Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Properties**.

Set the following property values in the System Property \[sys\_property\] table.

<table id="table_pjm_z4l_j4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_vaccine\_sm.vaccine.management.booking.max\_distance

</td><td>

If there’s no appointment slot available at the user’s preferred center, it's the maximum distance, in miles, that is searched for an available vaccination location.

 The default value is **50**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.booking.distance\_unit

</td><td>

The unit of measurement for the distance considered for vaccine appointment mass booking. The options are **mi** and **km**.

 The default value is **mi**.

</td></tr><tr><td>

sn\_vaccine\_sm.vaccine.management.booking.max\_locations

</td><td>

If there’s no appointment slot available at the user’s preferred location, it's the maximum number of alternate locations that are searched for a vaccination. A higher value for this property increases the time that it takes to complete mass booking.

 The default value is **5**.

</td></tr></tbody>
</table>Role required: sn\_vaccine\_sm.admin and admin

## About this task

**Important:** Mass booking doesn’t currently support inventory-based scheduling.

## Procedure

1.  Create a temporary table.

    The table should be either:

    -   Extend sys\_user.
    -   The user field in the table should have a reference to the sys\_user.
2.  Import the following health history data for each user into the temporary table.

    -   User
    -   Preferred vaccination center
    -   Age group
    -   Allergies to medications, food, a vaccine component, or latex \(Yes/No\)
    -   Serious reaction or fainted or nearly fainted during or after vaccination \(Yes/No\)
    -   Seizures or history of brain or nervous system problems \(Yes/No\)
    -   Long-term health problem with heart disease, lung disease, asthma, kidney disease, metabolic disease like diabetes, anemia, or other blood disorder \(Yes/No\)
    **Note:** This data is required to book appointments for users. If users book the appointments in the self-service portal, the users provide this information at the time of booking. When a user with the admin role mass-books appointments for users, the data must be imported instead.

    For more information about importing data, see Import sets.

3.  Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Mass Booking Configurations** and click **New**.

4.  Enter a name to describe the users included in the configuration.

5.  In the **Program** field, select the vaccination program to book appointments for.

6.  In the **Table Name** field, select the temporary table that you created.

7.  In the following fields, select the corresponding column from the temporary table to map the user data from the temporary table to the user's appointment.

    -   **Health history**
    -   **Vaccine reaction**
    -   **Age group**
    -   **Preferred center**
    -   **User**
    -   **Long term health issues**
    -   **Allergies**
8.  In the **Conditions** field, add filter conditions to define which users to book appointments for.

9.  To complete the configuration, click **Submit**.

    -   The configuration is saved but the appointments aren’t scheduled yet.
    -   If a consumer or patient record doesn’t exist for any user that has an appointment is booked, these records are created for the user.

## What to do next

When you're ready to schedule the appointments, return to the configuration record and click **Process Booking**.

**Note:** Whenever you process a booking, a new record gets created on the **Mass Booking Jobs** tab. Use this tab to view the progress of the scheduled appointments. For example, you can view the number of total appointments booked, appointments booked in a preferred center, the number of bookings failed for users, and so on.

**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

