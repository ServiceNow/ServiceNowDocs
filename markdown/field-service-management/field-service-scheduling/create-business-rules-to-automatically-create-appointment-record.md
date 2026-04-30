---
title: Create a business rule to automatically generate appointment records from catalog item variables
description: Automatically generate appointment records from catalog item variables using a business rule. Creating this automation ensures the appointment details provided by users through the Service Catalog appear on the appointment calendar.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a business rule to automatically generate appointment records from catalog item variables

Automatically generate appointment records from catalog item variables using a business rule. Creating this automation ensures the appointment details provided by users through the Service Catalog appear on the appointment calendar.

## Before you begin

Role required: admin

Ensure you have already created appropriate catalog item variables, such as appointment location or user contact.

## About this task

By creating a business rule, you can:

-   Automatically creates appointments as soon as users submit a service request.
-   Ensure user-provided appointment details \(like location and contact\) are immediately visible in the calendar.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Click **New**.

3.  In the **Name** field, enter your business rule name.

4.  Select your service table from the **Table** list.

5.  Select **Advanced**.

6.  On the **When to run** tab, in the **When** condition select `before` and select the **insert** check box.

    This ensures your rule runs before new records are inserted into the table.

7.  On the Advanced tab, add your condition in the **Condition** field.

    For example, add `current.variables.sn_appointment` in the **Condition** field.

8.  Enter the script in the **Script** field that you want to run when the defined condition is true.

    For example, add the below script to creates appointment record.

    ```
    (sn_apptmnt_booking.AppointmentBooking_Factory().getWrapperType(sn_apptmnt_booking.AppointmentBookingConstants.APPOINTMENT_BOOKING_IMPL);
        var sn_appointmentJSON = JSON.parse(sn_appointment);
        // creating an appointment <br>
        var appointmentId = helper.submitAppointmentFromPortal(sn_appointment, current, sn_appointmentJSON.config.opened_for, sn_appointmentJSON.config.location, current.short_description);
    )
    ```

9.  Click **Submit**.


## Result

The business rule is created.Whenever a customer submits a service request with an appointment variable, an appointment record automatically generates and appears in the appointment calendar.

