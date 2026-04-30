---
title: Configuring an appointment booking setting for Patient Support Services
description: Enable patients to book an appointment for the training requests conducted by nurse educators.Set up time windows for conducting a program task that patient can use to book appointments in the Patient Support Services application.Set up an appointment booking configuration for a service provided to patients within the program tasks.Create or modify different schedules on a day level when booking appointments for a program task. The appointments can be scheduled at different time slot of a day, such as morning, afternoon, or evening.Display a menu item to select appointments when booking or rescheduling an appointment for Patient Support Services on a patient portal.
locale: en-US
release: zurich
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring an appointment booking setting for Patient Support Services

Enable patients to book an appointment for the training requests conducted by nurse educators.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

In the Patient Support Services application, an appointment is booked for scheduling training requests included within a program service. For completing a program service item, a program task is created in the application.

The Patient Support Services application uses the Appointment Booking plugin \(com.snc.appointment\_booking\) to create an appointment record in the Appointment \[sn\_hcls\_appointment\] table. The appointment record is created for a program task that requires appointment booking. The plugin is automatically activated after your administrator installs the Patient Support Services application. For more information about the Appointment Booking feature, see [Appointment booking components](https://www.servicenow.com/docs/access?context=appointment-booking-components&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

As a user with the sn\_patientservice.admin role, you configure the following appointment booking settings:

1.  [Configure an appointment booking setting in Patient Support Services](pss-appt-booking-setup.md#).
2.  [Configure an appointment booking service setting in Patient Support Services](pss-appt-booking-setup.md#).

    **Note:** The appointment booking feature requires configuration for a program task that offers scheduled appointments. A service configuration includes settings that apply only to that specific service.

3.  Optional: [Configure a day-level appointment booking setting in Patient Support Services](pss-appt-booking-setup.md#).
4.  [Display an appointment booking window on a patient portal](pss-appt-booking-setup.md#).

**Related topics**  


[Booking appointments for Patient Support Services](pss-booking-appt-patient.md)

## Configure an appointment booking setting in Patient Support Services

Set up time windows for conducting a program task that patient can use to book appointments in the Patient Support Services application.

### Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Set the application scope to Patient Support Services using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Role required: sn\_patientservice.admin

### About this task

By default, the application includes the **Program service appointment** setting for a program task.

### Procedure

1.  Navigate to **All** &gt; **Patient Support Services** &gt; **Administration** &gt; **Appointment booking settings**.

2.  In the Appointment Booking Configuration list, either configure an existing setting or create a new one.

    -   Select an existing configuration in the Appointment Booking Configuration list.
    -   Create a new configuration by clicking **New** in the Appointment Booking Configuration list.
3.  On the form, verify the default field values for an existing configuration, or fill in the values for a custom configuration.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the configuration.

</td></tr><tr><td>

Task Table

</td><td>

Task table for which the appointment is created.

 The Patient service training \[sn\_patientservice\_training\_task\] table is the default table for the Patient Support Services training tasks.

</td></tr><tr><td>

Availability Method

</td><td>

Method to determine the appointment availability.

 An availability method is one of the following types:

-   **Number of appointments per slot**

Specific number of appointments per time slot. This method uses a specified number of available appointments per time window. The actual number of appointments is specified in the appointment service configuration. For example, if the administrator specifies 10 appointments per window, then each appointment window has 10 available appointments. The number of available appointments for an appointment window decreases by one each time an appointment within that window is booked.

-   **Scripted**

Script to determine the number of available appointments per time window.

</td></tr><tr><td>

Advanced Calendar view for Portal

</td><td>

Option to display the advanced calendar view for available appointments in the Select Appointment window on the patient portal.

 The advanced calendar view displays appointments categorized in different time slots of the day, such as morning, afternoon, and evening.

</td></tr><tr><td>

Active

</td><td>

Option for activating the application configuration and enabling the appointment booking.

</td></tr><tr><td>

Auto acceptance

</td><td>

Option to enable the auto-acceptance of the training tasks by an agent.

 For Patient Support Services, clear the Auto acceptance check box because the appointment for a training task is booked by a patient.

</td></tr><tr><td>

Calendar View

</td><td>

View of the available appointments in the Select Appointment window on the patient portal for a single day or for a week.

</td></tr><tr><td>

Advanced Calendar view for Portal

</td><td>

Advanced view of the available appointments in the Select Appointment window on the patient portal.

</td></tr><tr><td>

Script

</td><td>

Script used to determine the number of available appointments. This field appears only when **Scripted** is selected from **Availability Method**.

</td></tr></tbody>
</table>4.  Save your changes.

    -   For an existing configuration, click **Update**.
    -   For a new configuration, click **Submit**.

### What to do next

[Configure an appointment booking service setting in Patient Support Services](pss-appt-booking-setup.md#).

## Configure an appointment booking service setting in Patient Support Services

Set up an appointment booking configuration for a service provided to patients within the program tasks.

### Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: sn\_patientservice.admin

### About this task

By default, the application includes the **Program service appointment config** setting for the services included within the Patient Support Services training tasks.

### Procedure

1.  Navigate to **All** &gt; **Patient Support Services** &gt; **Administration** &gt; **Appointment booking settings**.

2.  Click the link to the appointment booking configuration with which you want to associate the setting.

3.  Either configure an existing setting or create a new one.

    -   Select an existing configuration in the Appointment Booking Service Configuration related list.
    -   Create a new configuration by clicking **New** in the Appointment Booking Service Configuration related list.
4.  On the form, verify the default field values for an existing configuration, or fill in the values for a custom configuration.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable day level configuration

</td><td>

Option to configure different schedule on a day level when booking appointments.

</td></tr><tr><td>

Active

</td><td>

Activates appointment booking for the service.

**Note:** If deactivated, customers cannot schedule appointments for the service but can still create work orders.

</td></tr><tr><td class="sub-head" colspan="2">

General Information

</td></tr><tr><td>

Name

</td><td>

Name to identify the service configuration.

</td></tr><tr><td>

Configuration

</td><td>

Name of the appointment booking configuration associated with this service. This field is automatically set to the selected appointment booking configuration.

</td></tr><tr><td>

Availability Table

</td><td>

Table that is used to calculate appointment availability. The default is the Appointment \[sn\_hcls\_appointment\] table.

</td></tr><tr><td>

Holiday Schedule

</td><td>

Holiday schedule to use when determining appointment availability.

 Click the lookup icon \(![Lookup using list icon.](../image/lookup-using-list.png)\) and select a schedule from the Schedules list.

 The appointment booking feature evaluates the holiday schedule when determining the number of available appointments and excludes any day in the schedule that is set to **Exclude**. For more information, see [Holidays](https://www.servicenow.com/docs/access?context=c_Holidays&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td class="sub-head" colspan="2">

Catalog Information

</td></tr><tr><td>

Catalog Item

</td><td>

Service in the service catalog for which this appointment booking configuration is being created.

 Click the lookup icon \(![Lookup using list icon.](../image/lookup-using-list.png)\) and select a service from the Record Producers list.

 By default, the application includes the **Program service appointment** record producer for the **Program service appointment** configuration.

</td></tr><tr><td>

Location

</td><td>

Field in the record provider that determines the appointment location.

</td></tr><tr><td>

Timezone

</td><td>

Appointment window based on the **Timezone** field specified in the patient record or the location where the appointment for the training task is scheduled.

</td></tr><tr><td>

Appointment is mandatory

</td><td>

Option to make creating an appointment when requesting the service as a requirement.

</td></tr><tr><td>

User contact

</td><td>

Field on the record provider that determines who the appointment is being created for.

 A reference field that looks for a `sys_user` variable and sets the variable on the record producer; for example, **Patient**.

</td></tr><tr><td class="sub-head" colspan="2">

Booking

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments for each configured appointment time slot.

 The numeric value you enter determines the number of available appointments that are displayed on the Select Appointment window.

</td></tr><tr><td>

Lead time

</td><td>

Number of hours or days from the current time after which an appointment can be booked for this service.

</td></tr><tr><td>

Future bookable max days

</td><td>

Number of days prior to the current day for which an appointment can be booked for this service.

</td></tr><tr><td>

Reschedule/Cancel by time

</td><td>

Number of hours or days prior to an appointment start time that are required for an appointment to be canceled or rescheduled.

 If a patient attempts to cancel or reschedule an appointment within this number of hours, the **Cancel** button is not available.

</td></tr><tr><td class="sub-head" colspan="2">

Appointments

</td></tr><tr><td>

Appointment window

</td><td>

Duration of the appointment window.

**Note:** Allow enough time for the training to be started and completed within this window.

</td></tr><tr><td>

Work duration

</td><td>

Amount of time required to complete all tasks created by the record producer.

</td></tr><tr><td>

Travel duration \(round trip\)

</td><td>

Average travel time required for an agent. This field is not used in Patient Support Services.

</td></tr><tr><td class="sub-head" colspan="2">

Daily Schedule

</td></tr><tr><td>

Bookable days

</td><td>

Days of the week for which appointments can be booked.

</td></tr><tr><td>

Daily start time

</td><td>

Earliest start time for an appointment window in a workday.

</td></tr><tr><td>

Daily end time

</td><td>

Latest end time for an appointment window in a workday.

</td></tr><tr><td>

Include daily break

</td><td>

Option for scheduling a break for each bookable day.

 If you select the **Include daily break** check box, you can then specify the break start and end times in the boxes that appear.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>5.  Save your changes.

    -   For an existing configuration, click **Update**.
    -   For a new configuration, click **Submit**.

## Configure a day-level appointment booking setting in Patient Support Services

Create or modify different schedules on a day level when booking appointments for a program task. The appointments can be scheduled at different time slot of a day, such as morning, afternoon, or evening.

### Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

1.  [Configure an appointment booking setting in Patient Support Services](pss-appt-booking-setup.md#).
2.  [Configure an appointment booking service setting in Patient Support Services](pss-appt-booking-setup.md#).

Role required: admin

### About this task

You can create a single or multiple day level configurations for each program task that requires an appointment booking.

### Procedure

1.  Navigate to **All** &gt; **Patient Support Services** &gt; **Administration** &gt; **Appointment booking settings**.

2.  Click the link to the appointment booking configuration with which you want to associate the setting.

3.  Click the link to the appointment booking service configuration for which you want to configure different appointment schedules.

4.  Select the **Enable day level configuration** check box.

5.  In the Appointment Booking Day Configuration related list, click **New**.

6.  On the form, fill in the fields.

7.  <table id="table_lws_gcg_fqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the day-level configuration, such as Morning, Afternoon, or Evening.

</td></tr><tr><td>

Active

</td><td>

Option for activating the appointment slot.

</td></tr><tr><td>

Start date

</td><td>

Start date of the appointment booking window.

</td></tr><tr><td>

End date

</td><td>

End date of the appointment booking window.

</td></tr><tr><td>

Daily start time

</td><td>

Earliest start time for an appointment window in a workday.

</td></tr><tr><td>

Daily end time

</td><td>

Latest end time for an appointment window in a workday.

</td></tr><tr><td>

Service configuration

</td><td>

Name of the service configuration for which you are scheduling configurations on a day level.

</td></tr><tr><td>

Work duration

</td><td>

Amount of time required to complete all tasks created by the record producer.

</td></tr><tr><td>

Travel Duration \(round trip\)

</td><td>

Estimated value of the average travel time required \(round trip\) for the agent performing the task. This field is not applicable to Patient Support Services.

</td></tr><tr><td>

Appointment window

</td><td>

Duration of the appointment window.

**Note:** Allow enough time for the training to be started and completed within this window.

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments for each configured appointment time slot.

 The numeric value you enter determines the number of available appointments that are displayed on the Select Appointment window.

</td></tr><tr><td>

Include daily break

</td><td>

Option for scheduling a break for each bookable day.

 If you select the **Include daily break** check box, you can then specify the break start and end times in the boxes that appear.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr></tbody>
</table>8.  Click **Submit**.


## Displaying appointment booking window on a patient portal

Display a menu item to select appointments when booking or rescheduling an appointment for Patient Support Services on a patient portal.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

By default, the **Program service appointment** record producer is available for booking appointments associated with Patient Support Services. You can use the default record producer to enable patients to book appointments or create your own record producer.

As an administrator, you can include the record producer for appointment booking in a service  catalog and display the service  catalog  as a module on a patient portal. Patients can then use the module to book appointments for a training request.

For more information, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Set up a service catalog](https://www.servicenow.com/docs/access?context=t_SetUpAServiceCatalog&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) . 

