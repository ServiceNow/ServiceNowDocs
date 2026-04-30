---
title: Configure variable in service catalog record producer for appointment booking
description: Create variables for the catalog item attributes within the appointment booking service configuration. Configuring distinct variables for location and user contact, enables you to specify both the location and contact details when booking an appointment on the calendar.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configure variable in service catalog record producer for appointment booking

Create variables for the catalog item attributes within the appointment booking service configuration. Configuring distinct variables for location and user contact, enables you to specify both the location and contact details when booking an appointment on the calendar.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Click the desired record producer.

3.  In the **Variable** related list, click **New**.

4.  On the form, fill in the fields.

5.  <table id="table_t54_b3k_lzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

This is a read-only field and is set by default based on the application scope.

</td></tr><tr><td>

Type

</td><td>

Supported variable types for this catalog item record producer.If you use unsupported variables, Service Catalog might not integrate the data in the right format.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item that uses the variable.

</td></tr><tr><td>

Order

</td><td>

Placement order of the variable on the catalog item page. You organize the variables from top to bottom, and from the least to the greatest order value.For example, a variable with an order value of 1 is placed ahead of other variables with higher-order values.

</td></tr><tr><td>

Active

</td><td>

This is a read-only field and is enabled based on the Publish, Retire, or Edit actions.

</td></tr><tr><td>

Mandatory

</td><td>

Option for making the variable mandatory as part of the ordering process.**Note:** This behavior is applicable only on a page load. You can change it by using client APIs.

</td></tr><tr><td>

Question

</td><td>

Question that you can ask users who are ordering the catalog item to obtain related information.

</td></tr><tr><td>

Name

</td><td>

Name to identify the question.**Note:** If this field is empty, its value is auto-populated based on the Question field for all variable types except Break, Container Split, and Container End.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when users point to the variable. Enter a brief note to describe the purpose of the question.

</td></tr><tr><td>

Example Text

</td><td>

Question field hint that appears before a user enters a value. You can use a hint for the following variables:-   Email
-   URL
-   Single-Line Text
-   Multiline Text
-   Wide Single-Line Text


</td></tr><tr><td>

Type Specification

</td><td>

Values specific to the type of variables.

</td></tr></tbody>
</table>6.  Click **Submit**.

    Repeat steps 3 through 5 to create additional variables for the same catalog item record producer.


## Result

The service catalog record producer creates the variable record in the selected table. The default table is wm\_order.

## What to do next

Add this variable entry in the Appointment booking table to ensure that it’s visible on the calendar for users when booking an appointment. For more information, see [Create business rules to automatically create an appointment record for the catalog item variable](create-business-rules-to-automatically-create-appointment-record.md)

**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

