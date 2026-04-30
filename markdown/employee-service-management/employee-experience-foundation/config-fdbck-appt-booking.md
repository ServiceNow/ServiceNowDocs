---
title: Configure feedback for appointment booking
description: Create a feedback definition for appointment booking so employees can provide feedback for completed appointments.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Appointment Booking, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure feedback for appointment booking

Create a feedback definition for appointment booking so employees can provide feedback for completed appointments.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

## About this task

The appointment booking experience already contains two feedback definitions for Employee Center Pro and Employee Center Pro Kiosk.

You can modify the feedback definitions provided with the plugin, or create your own. For more information about the feedback feature, see [Integrated experience and service feedback](../concept/ex-fdback-ovrvw.md).

You can modify the number of times a user can submit feedback in a single session by configuring the **Overlay session limit** field in the feedback configuration. The **Overlay session limit** value is set to 5 by default. For more information about feedback configurations, see [Set up the feedback configuration](config-employee-ex-fdbck.md).

If you create a custom feedback definition for appointment booking, ensure that you deactivate other feedback definitions that are on the same portal.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Experience and Service Feedback** &gt; **Feedback Definitions**.

2.  On the Feedback Definitions list, select **New**.

3.  On the Feedback definition form, enter the following field values.

<table><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Feedback type

</td><td>

Service - workflow

</td></tr><tr><td>

Widget mode

</td><td>

Modal

</td></tr><tr><td>

Channel

</td><td>

Portal

</td></tr><tr><td>

Portals

</td><td>

-   Employee Center
-   Employee Center Pro Kiosk
 **Note:** You can select one or both portals based on your requirement.

</td></tr></tbody>
</table>4.  On the Page selection tab, in the **Included pages** field, select the following pages.

    -   my\_appointments
    -   appointment\_details
    You can fill in the remaining fields based on your preference. For a description of the field values, see [Feedback definition form](../reference/fdbck-dfnition-record.md).

5.  Save the record.

6.  In the Trigger conditions related list, select **New**.

7.  On the Trigger condition form, enter the following values.

    |Field|Value|
    |-----|-----|
    |Table|Walk-up Appointment \[wu\_appointment\]|
    |User field|Opened by|
    |Trigger randomly|Selected|
    |Probability \(%\)|100|

8.  In the **Repeat Interval** field, ensure that all values are set to `00`.

9.  In the **Condition** field, enter the following values.

    |Field|Value|
    |-----|-----|
    |-- choose field --|State|
    |-- oper --|is|
    |-- value --|Closed Complete|

10. Save the record.


