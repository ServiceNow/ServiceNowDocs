---
title: Configure variable time slots for appointment booking
description: Configure variable time slots for appointment booking in a walk-up location by defining rules and configurations.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Variable time slots for appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Configure variable time slots for appointment booking

Configure variable time slots for appointment booking in a walk-up location by defining rules and configurations.

## Before you begin

Role required: appointment\_booking\_admin or admin

## About this task

To use the appointment booking feature, administrators must create a configuration for each service or queue location that is available to walk-up customers. Service configurations are created within the Walk-up Experience application configuration, as part of the Appointment Booking application.

## Procedure

1.  Navigate to **All** &gt; **Walk-up Experience** &gt; **Administration** &gt; **Appointment Configurations**.

2.  Create or modify Appointment Booking Configuration.

    -   To create a new configuration for appointment booking, select **New**.
    -   To modify an existing configuration, select the configuration from the list.
    **Note:** For more information on creating or modifying appointment booking configuration for Walk-up Experience and field-related information, see [Create or modify a Walk-up Experience appointment booking service configuration](configure-walkup-appointments.md).

3.  Select the **Enable advanced configurations** check box.

    The **Advance Configurations** and **Service Configuration Rules** tabs appear in the related list of the Appointment Booking Service Configuration form.

4.  Click the **Service Configuration Rules** tab, and create or modify an existing rule.

    -   To create a new rule, click **New**.
    -   To modify an existing rule, select the configuration from the list.
5.  On the Service Configuration Rule form, fill in the fields and click **Submit**.

    For more information on the fields, see [Create appointment booking service configuration rules](https://www.servicenow.com/docs/access?context=create-appt-booking-service-config-rules&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

    **Note:** The **Task Table** and **Task Conditions** fields are not applicable for Walk-up Experience.

6.  Click the **Advance Configurations** tab, and create or modify a configuration.

    -   To create a new configuration, click **New**.
    -   To modify an existing configuration, select the configuration from the list.
7.  On the **Advance Configurations** form, fill in the fields and click **Submit**.

    For more information on the fields, see [Create appointment booking advanced configuration](https://www.servicenow.com/docs/access?context=appintment-booking-day-level-config&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

8.  Click **Submit**.


## What to do next

You must map the defined advance configurations with the defined service configuration rule for a location. Use the Reasons for Visit related list on the Walk-up Location Queue form. For more information, see [Create or modify Walk-up Experience locations](configure-walkup-location.md).

**Parent Topic:**[Configure Variable time slots for appointment booking](../concept/variable-time-slots.md)

