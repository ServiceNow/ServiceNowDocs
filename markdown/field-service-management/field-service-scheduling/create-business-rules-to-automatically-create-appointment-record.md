---
title: Create business rules to automatically create an appointment record for the catalog item variable
description: Create a before insert business rule on the service table to automatically add a variable for service catalog in the appointment booking table. This ensures that the variable record is visible on the appointment calendar for users when booking an appointment.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create business rules to automatically create an appointment record for the catalog item variable

Create a before insert business rule on the service table to automatically add a variable for service catalog in the appointment booking table. This ensures that the variable record is visible on the appointment calendar for users when booking an appointment.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Click **New**.

3.  In the **Name** field, enter your business rule name.

4.  Select your service table from the **Table** list.

5.  Select **Advanced**.

6.  On the **When to run** tab, in the **When** condition select `before` and select the **insert** check box.

    This action specifies that the business rules should run before the insert.

7.  On the Advanced tab, add your condition in the **Condition** field.

    For example, add `current.variables.sn_appointment` in the **Condition** field.

8.  Enter the script in the **Script** field that you want to run when the defined condition is true.

    For example, add the following script to creates appointment record.

    ```
    (sn_apptmnt_booking.AppointmentBooking_Factory().getWrapperType(sn_apptmnt_booking.AppointmentBookingConstants.APPOINTMENT_BOOKING_IMPL);
        var sn_appointmentJSON = JSON.parse(sn_appointment);
        // creating an appointment <br>
        var appointmentId = helper.submitAppointmentFromPortal(sn_appointment, current, sn_appointmentJSON.config.opened_for, sn_appointmentJSON.config.location, current.short_description);
    )
    ```

9.  Click **Submit**.


**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

