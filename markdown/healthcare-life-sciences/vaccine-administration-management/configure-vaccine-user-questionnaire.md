---
title: Configure an appointment reminder and pre-appointment questionnaire
description: By default, appointment reminders aren’t sent to the user. To enable appointment reminders, you must configure the appointment reminder in the appointment configuration record. You can also configure the pre-appointment questionnaire for users.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure an appointment reminder and pre-appointment questionnaire

By default, appointment reminders aren’t sent to the user. To enable appointment reminders, you must configure the appointment reminder in the appointment configuration record. You can also configure the pre-appointment questionnaire for users.

## Before you begin

Role required: admin

## About this task

The appointment reminder sends a reminder email and a pre-appointment questionnaire to the user at a specified time.

## Procedure

1.  To configure the appointment reminder.

    1.  Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Appointment Configurations**.

    2.  Open the Schedule Vaccine Appointment record.

    3.  In the **Appointment reminder** field, select the reminder time.

        **Note:** If the field doesn't appear on the form, a user with the admin role must configure the form layout to include it. In the form header, click the form context menu icon \(![Form context menu icon.](../image/hamburger-icon.png)\). Navigate to **Configure** &gt; **Form Layout** and move the **Appointment reminder** field to the Selected list, then click **Save**.

        By default, appointment reminders aren’t sent to the user. If you want the user to receive the email reminder, configuration of both the appointment reminder and the pre-appointment questionnaire is required.

    4.  Click **Update**.

2.  Configure the pre-appointment questionnaire.

    1.  Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Pre-appointment Questionnaire**.

        The Pre-appointment Questionnaire record producer is displayed.

    2.  In the Variable Sets related list, open the Pre-vaccination screening record.

        The *Pre-vaccination screening* variable set is displayed.

    3.  In the Variables related list, create or update variables for the questionnaire.

        For details on how to configure a variable, see [Service catalog variables](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

        **Important:** Don’t configure the *task\_id* and *is\_portal* variables.

    4.  Click **Update**.


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

